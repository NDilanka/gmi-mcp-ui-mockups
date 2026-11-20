# Day 1 — Acan v4 Dark Spatial Hero Prompt (Full-Bleed Tactile Workbench)

## Why v4 (Pivot from v3)
v3 nailed typography accuracy and warm-graphite restraint, but still sat inside a classic 3-pane SaaS layout (left rail + center + right inspector) with flat dark cards.
v4 breaks out of the 3-pane grid completely into a **100% full-bleed infinite spatial canvas** crafted like a **Teenage Engineering / Dieter Rams anodized hardware instrument** for collaborative, agentic software building:
- **Zero sidebars, zero nested boxes-in-boxes, 45% open breathing canvas.**
- **Tactile physical materiality:** powder-coated obsidian-graphite drafting mat with ultra-subtle micro-dot grid, chamfered matte anodized aluminum floating modules with razor-thin top catch-lights, soft diffused drop shadows, silkscreen monospace micro-labels, and physical hardware keycaps.
- **Richer Acan state:** floating codebase circuit topology (`acan-scan`, `acan-core`, `acan-git`, `acan-server`) directly on the grid with live worker wakes (`w1` mint, `w2` amber), a multiplayer collaborator cursor (`AK`) actively inspecting the canvas, a floating **generative UI instrument card** combining a clean 5-line Rust `Settlement` diff with a miniature Braun/TE telemetry LED + sparkline meter (`14/14 checks`, `risk 0.04`), and three sculptural physical keycaps (`1 Serialize`, `2 Split`, `3 Inspect`) floating cleanly in open space.
- **Minimal floating chrome:** tiny top-left `ACAN` hardware pill with a single amber LED dot, top-right machined multiplayer avatars (`ND`, `AK`, `MR`) + `⌘K`, and a slim floating bottom-center Teenage Engineering command dock (`MAP` · `LIVE` · `DIFF` + quiet order bar + single orange circular hardware trigger).

---

## Target Models (Sequential, Quote-First)
1. `gpt-image-2.6-sunburst-generate` — `size: "1536x1024"`, `quality: "max"`, `n: 1` (est. ~$0.1745) -> `outputs/v4-hero-sunburst-max.png`
2. `gemini-nano-banana-2.1` — `aspect_ratio: "16:9"`, `image_size: "2K"`, `image_output_format: "png"`, `thinking_level: "high"`, `n: 1` (est. ~$0.0655) -> `outputs/v4-hero-nano-banana-2k.png` (+ `-alt.png` if 2 items returned)

---

## Prompt (Exact Text Passed to Both Models)

```text
Ultra-crisp, flat 2D screenshot of a visionary desktop developer instrument called Acan, designed with Teenage Engineering OP-1 Field and Dieter Rams industrial design craft combined with a full-bleed infinite spatial canvas. No perspective tilt, no laptop mockup, no browser chrome, no 3-pane SaaS layout, no sidebars, no chat panel.

CANVAS & MATERIALITY:
The entire frame is a single continuous, full-bleed matte anodized obsidian-graphite drafting surface (#0E0E10) with an ultra-subtle micro-dot architectural grid (#1B1B1F) and gentle top-down studio light falloff. Generous open breathing room: at least 45% of the screen is calm, unobstructed dark dot-grid canvas. Floating modules feel like precision-machined matte powder-coated aluminum and dark graphite hardware resting cleanly above the mat, with razor-thin top-edge specular bevel highlights, soft diffused ambient shadows, and zero cluttered nested borders. Color palette is 90% matte charcoal (#151518, #1C1C20), warm titanium grey (#8A8882), and soft bone white (#ECEAE4), accented sparingly with only three purposeful hardware signal inks: Braun signal orange (#E87A35), oscilloscope mint (#4DC496), and cool cobalt (#6FA8DC).

MINIMAL FLOATING CORNER CHROME (ultra-compact, zero clutter):
- Top-left floating pill: tiny glowing signal-orange LED dot, crisp silkscreen monospace text "ACAN", subtle divider, "v1".
- Top-right floating group: three minimal machined circular collaborator tokens labeled "ND", "AK", "MR", plus a tiny physical keycap "⌘K".
- Bottom-center floating Teenage Engineering tactile dock: a slim recessed matte gunmetal hardware bar with three tiny segmented mode tabs ("MAP", "LIVE" active with hairline amber underline, "DIFF"), a quiet input prompt "Issue order...", and one small circular matte signal-orange hardware button on the right end.

SPATIAL CONTENT FLOATING DIRECTLY ON THE CANVAS (only two calm focal islands separated by generous open space):

1. LEFT-CENTER — FLOATING SPATIAL CIRCUIT TOPOLOGY (placed directly on the dot-grid canvas, NO enclosing box or card border):
Four crisp, precision-machined rectangular hardware nodes connected by clean orthogonal 1px titanium circuit-trace lines:
- "acan-scan" (tiny mint status LED)
- "acan-core" (central hub, subtle chamfered edge, slightly elevated)
- "acan-git" (connected below-right)
- "acan-server" (connected right)
Two live autonomous workers moving along the traces:
- A small glowing oscilloscope-mint pulse dot labeled "w1" gliding smoothly along the trace from "acan-scan" into "acan-core" with a soft fading light wake.
- A small glowing signal-orange ringed dot labeled "w2" paused neatly at a miniature precision gate marker between "acan-core" and "acan-git" with quiet micro-text "held".
Multiplayer presence on the canvas: a crisp cool-cobalt pointer cursor with a small chamfered tag "AK" hovering near "acan-core", surrounded by a whisper-thin cobalt selection corner bracket.

2. RIGHT-CENTER — FLOATING GENERATIVE UI INSTRUMENT MODULE + PHYSICAL KEYCAP LATCH:
A single calm, precision-machined matte graphite hardware instrument card floating over the grid with generous internal padding (zero walls of text, zero cluttered toolbars):
- Top silkscreen strip (small tracked monospace, titanium grey): "CLASH · acan-core/clash.rs" on the left, "w2 · 01" on the right.
- Clean, breathable 5-line Rust diff block set in crisp monospace on a subtly recessed dark anodized display well (#111114), with generous line height and zero clipped characters:
  pub enum Settlement {
      Narrow { task: TaskId },
  +   Serialize { first: TaskId, then: TaskId },
      SplitAtContract { owner: TaskId, contract: String },
  }
  The added line has a subtle oscilloscope-mint left accent bar and faint mint tint.
- Directly below the code well, a sleek Dieter Rams / Teenage Engineering generative telemetry strip: a crisp minimalist miniature waveform/sparkline graph in oscilloscope mint alongside a row of tiny circular LED indicator dots (12 mint lit, 2 dim) and clean micro-readouts "14/14 checks" and "risk 0.04".
- Floating cleanly below the instrument module with open canvas gap: three sculptural, chamfered physical Teenage Engineering hardware keycaps side by side:
  [ 1 ] Serialize   (subtle signal-orange illuminated rim and orange keycap number)
  [ 2 ] Split       (matte anodized graphite)
  [ 3 ] Inspect     (matte anodized graphite)

TYPOGRAPHY & QUALITY:
Every single letter, symbol, code identifier, brace, and number must be razor-sharp, spelled 100% accurately, cleanly aligned, with zero artifacts, zero garbled text, zero prompt numbers leaked onto the screen, and serene museum-grade industrial-design restraint.
```
