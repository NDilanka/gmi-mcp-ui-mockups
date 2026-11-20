# GMI Cloud MCP guardrails (paste into AGENTS.md or CLAUDE.md)

## GMI Cloud MCP rules

Server: `https://mcp.gmicloud.ai/mcp` (droid server name: `gmi`)

These rules apply to any agent that calls GMI MCP tools for paid generation.

1. Find models with `search_models`. Call `get_model` for every model before any estimate or submit call. Read its schema and price from that response.
2. Use exact, case-sensitive enum values from the `get_model` schema. Do not guess, lowercase, or rename enum values.
3. Call `estimate_generation` for every planned generation. Show the quoted cost and the full parameter set to the human.
4. Wait for explicit human approval of that quote before calling `submit_generation`. Approval covers only that quote.
5. Never auto-retry a `submit_generation` call. If a submit errors or times out, call `list_generations` to check whether it ran. Re-submit only after a human says so.
6. For local files, use the `upload_media` three-step flow exactly as its tool schema documents. Do not skip or reorder steps.
7. After each run, call `list_generations`. Record the request ID, model ID, and cost in the run log.
8. If a quote exceeds the budget the human approved, stop and ask.
9. Do not state a cost, latency, or output quality that the live run did not return.
