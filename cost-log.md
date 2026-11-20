# Day 1 Cost Log: Acan UI Mockups (Rounds 1 to 4)

Folder: `day1-acan-ui-mockups/`. Paths below are relative to this folder.

Run date: 2026-11-20 (UTC, from `created_at` in `list_generations`).

Quoted costs are list price before any org discount, from `estimate_generation`. Actual per-run charges are not returned by `list_generations` or `get_generation`; totals are reconciled against `get_account_summary`.

## Sources

| Figure | Source | Status |
|---|---|---|
| Request IDs, models, statuses, timestamps | `list_generations` and `submit_generation` responses in this session (14 entries total) | Verified |
| Failure reason and two-image returns | `get_generation` and `submit_generation` media arrays | Verified |
| Output-to-request mapping | Rounds 1 to 2 + Edit 1 verified by SHA-256; Rounds 3 to 4 downloaded directly from each sequential job's media URLs | Verified |
| Quoted cost per run | `estimate_generation` before each submit | Verified as quotes, not per-run charges |
| Output dimensions | PNG headers of files in `outputs/` and `outputs/x-ready/` | Verified |
| Account balance and promo credit progression | `get_account_summary` reads across the session, final settled read after Round 4 | Verified |
| Per-run actual charge | Not returned by any MCP tool | Not verified individually |

## Account snapshot

| Point | balance_usd | promotion_credit_usd | Delta from prior | Source |
|---|---|---|---|---|
| Initial | 0.00 | 49.58 | - | Session start read |
| Mid-run (during Round 1/2) | 0.00 | 49.21 | -0.37 | Session record |
| Before Edit 1 (after 8 successful runs) | 0.00 | 48.83 | -0.38 (-0.75 cumul.) | Session record |
| After Edit 1 (9 successful runs) | 0.00 | 48.74 | -0.09 (-0.84 cumul.) | `get_account_summary` |
| After Round 3 settled (11 successful runs) | 0.00 | 48.49 | -0.25 (-1.09 cumul.) | `get_account_summary` |
| After Round 4 settled (13 successful runs) | 0.00 | 48.25 | -0.24 (-1.33 cumul.) | `get_account_summary` |

## Round one (v1)

| Run | Model ID | Request ID | Created (UTC) | Status | Quoted list cost (USD) | Output file | Notes |
|---|---|---|---|---|---|---|---|
| 1, Direction A | gpt-image-2-generate | 7ace9196-be40-47d5-b04d-dfe5e54c3b31 | 03:52:49 | success | 0.16664 | `outputs/dir-a-swiss-light-gpt-image-2.png` (1536 x 1024) | `size` 1536x1024, `quality` high, `output_format` png, `n` 1. |
| 2a, Direction B, failed | reve-2-1 | eb0db1b4-f81f-4c00-9d05-32603f170fc8 | 03:52:49 | failed | 0.20 | None | Submit returned `upstream_unavailable`. Terminal 503 (`unconditional drop overload`). Not retried. Excluded from successful total. |
| 2b, Direction B | gpt-image-2-generate | eaa225a3-3272-463a-9d11-19ae485e615e | 03:58:12 | success | 0.16664 | `outputs/dir-b-dark-instrument-gpt-image-2.png` (1536 x 1024) | Spend guard $0.25 passed. Submitted once. |
| 3, Direction C | gemini-3.1-flash-image | 181f44bf-b712-458b-b51b-ef0a818d1ea0 | 03:52:50 | success | 0.104 | `outputs/dir-c-split-dispatch-gemini-3-1-flash.png` (2752 x 1536) | `aspect_ratio` 16:9, `image_size` 2K. Replaced `flux-kontext-pro` after `get_model` showed text-only schema. |

## Round two (v2)

Five requests, all succeeded. Per-request quotes for Round 2 were combined into the verified subtotal below.

| Request ID | Model ID | Created (UTC) | Status | Output file(s) |
|---|---|---|---|---|
| 1f5940e6-f358-4611-95b0-c0e678fa4bdc | gemini-nano-banana-2.1 | 04:13:03 | success | `outputs/v2-p1-board-nano-banana-2k.png` (1376 x 768). Returned two images on `n=1`; item 1 (4,315,050 B) not saved. |
| 70f3825b-10b6-491b-9ba4-a01c43829ce3 | gpt-image-2.6-sunburst-generate | 04:13:26 | success | `outputs/v2-p1-board-sunburst-xhigh.png` (1536 x 1024) |
| 0ac23d69-f618-40ad-8e5c-51e93c405aea | gpt-image-2.6-sunburst-generate | 04:13:26 | success | `outputs/v2-p3-receipt-sunburst-xhigh.png` (1536 x 1024) |
| b3b75b6b-c3e0-4d26-8c21-a9f0f92d6133 | gpt-image-2.6-sunburst-generate | 04:13:26 | success | `outputs/v2-p2-map-sunburst-xhigh.png` (1536 x 1024) |
| 178550b4-82ea-47d6-88a-457e67246225 | gemini-nano-banana-2.1 | 04:14:05 | success | `outputs/v2-p2-map-nano-banana-2k.png` (1376 x 768). Returned two images on `n=1`; item 1 (4,193,356 B) not saved. |

## Edit pass 1

| Run | Model ID | Request ID | Created (UTC) | Status | Quoted list cost (USD) | Output file | Notes |
|---|---|---|---|---|---|---|---|
| Edit 1 | gpt-image-2.6-sunburst-edit | 0832c314-5b91-45c0-97df-b19a1ba1b51b | 04:23:45 | success | 0.088343 | `outputs/v2-p2-map-sunburst-edited.png` (1536 x 1024) | Input uploaded with 3-step `upload_media`. Output kept backticks around paths and dropped keycap brackets, prompting the move to a dark v3 hero. |

## Round three (v3 dark hero, sequential)

| Run | Model ID | Request ID | Status | Quoted list cost (USD) | Output file(s) | Notes |
|---|---|---|---|---|---|---|
| v3-1 | gpt-image-2.6-sunburst-generate | 75e2f4b5-29ed-4162-ab9b-65d0f38f4ee8 | success | 0.174545 | `outputs/v3-hero-sunburst-max.png` (1536 x 1024, 1,391,619 B) | `size` 1536x1024, `quality` max, `n` 1. Zero typos in Rust diff, still 3-pane layout. |
| v3-2 | gemini-nano-banana-2.1 | 584e95ac-bffa-40cd-978b-022709110057 | success | 0.0655 | `outputs/v3-hero-nano-banana-2k.png` (1376 x 768, 1,067,997 B) and `outputs/v3-hero-nano-banana-2k-alt.png` (2752 x 1536, 4,327,596 B) | `aspect_ratio` 16:9, `image_size` 2K, `thinking` high, `n` 1. Returned two images; item 0 is a smaller draft and item 1 is the clean 2752x1536 render. |

Round 3 settlement check: combined quote was $0.240045 and promo credit dropped $0.25 ($48.74 to $48.49), consistent with single-image billing on `gemini-nano-banana-2.1`.

## Round four (v4 full-bleed spatial workbench, sequential)

| Run | Model ID | Request ID | Created (UTC) | Status | Quoted list cost (USD) | Output file(s) | Notes |
|---|---|---|---|---|---|---|---|
| v4-1 | gpt-image-2.6-sunburst-generate | 52249152-91d3-4684-aec2-8dda455d15d9 | 05:10:15 | success | 0.17257 | `outputs/v4-hero-sunburst-max.png` (1536 x 1024, 1,339,213 B) | `size` 1536x1024, `quality` max, `n` 1. Cleanest minimal UI runner-up. X-ready 1600x900 export in `outputs/x-ready/post3-v4-sunburst-1600x900.png`. |
| v4-2 | gemini-nano-banana-2.1 | 505b4e56-2d61-4b77-b9a6-9a45e2011387 | 05:11:56 | success | 0.0655 | `outputs/v4-hero-nano-banana-2k.png` (1376 x 768, 1,090,051 B) and `outputs/v4-hero-nano-banana-2k-alt.png` (2752 x 1536, 4,133,277 B) | `aspect_ratio` 16:9, `image_size` 2K, `thinking` high, `n` 1. **Selected Day 1 hero** (`-alt.png`). X-ready 1600x900 export in `outputs/x-ready/post1-v4-nano-banana-1600x900.png`. |

Round 4 settlement check: combined quote was $0.23807 and promo credit dropped $0.24 ($48.49 to $48.25), again matching single-image billing on `gemini-nano-banana-2.1`.

## Totals

| Group | Generations | Quoted list cost (USD) | Basis |
|---|---|---|---|
| Round one, successful (Runs 1, 2b, 3) | 3 | 0.43728 | Per-run quotes |
| Round two, successful (5 requests) | 5 | 0.36545 | Derived subtotal |
| Edit pass 1 | 1 | 0.088343 | Quote |
| Round three, successful (v3-1, v3-2) | 2 | 0.240045 | Per-run quotes (0.174545 + 0.0655) |
| Round four, successful (v4-1, v4-2) | 2 | 0.23807 | Per-run quotes (0.17257 + 0.0655) |
| **Successful total** | **13** | **1.369188** | **Sum ($1.37 list)** |
| Failed Run 2a (quote only) | 1 | 0.20 | Quote; charge not returned |
| All quotes, including the failed run | 14 | 1.569188 | Sum |

## Promo credit reconciliation

- Promo credit moved from $49.58 to $48.25, a total settled drop of **$1.33** across all 4 rounds ($0.00 cash balance).
- Successful list-price quotes sum to **$1.369188** ($1.37), about 4 cents above the settled credit drop.
- Rounds 3 ($0.25 settled vs $0.240 quote) and 4 ($0.24 settled vs $0.238 quote) both confirm two things: billing settles asynchronously a minute or two after completion, and `gemini-nano-banana-2.1` only billed once per request even though it returned two media items on `n=1`.
- The earlier 5-cent gap occurred during Rounds 1 and 2 ($0.75 settled vs $0.803 quoted); the exact cause (such as an org discount or rounding) is not exposed by the API.
