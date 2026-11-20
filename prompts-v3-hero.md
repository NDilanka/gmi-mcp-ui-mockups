# Acan V1 Hero UI — Dark Tactile Minimalism + Living Spatial Canvas (v3)

Grounded in Acan's real `Look::Dark` warm-graphite palette and real domain vocabulary (`Order`, `Task`, `Clash`, `Settlement`, `NeedsYou`, `Receipt`, `acan-core`, `acan-intent`, `acan-git`, `acan-scan`, `acan-server`), fusing Dieter Rams / Teenage Engineering tactile hardware restraint with Zed/Delta 12px native desktop density and a whisper-quiet living 2D spatial workspace. Zero chat box.

## Hero Prompt (v3)

Ultra-high-craft native desktop developer application UI screenshot (16:9 widescreen) for a next-generation coding-agent control room called Acan. Visual direction fuses Dieter Rams and Teenage Engineering OP-1 Field tactile hardware minimalism with Zed and Delta.dev razor-sharp native desktop precision (tight 12px and 11px typography, zero oversized toy fonts, zero bloated web cards).

Color system and mood: Deep, calm, warm-matte graphite dark mode that screams for LESS attention. Primary canvas `#161615`, recessed side bays `#1c1c1a`, tactile flat control surfaces `#232320`, ultra-fine `1px` hairline structural dividers `#2e2e2b`. 92% of the screen stays quiet, low-contrast warm monochrome (`#e6e6e1` crisp soft-ivory primary text, `#8c8c86` quiet muted labels, `#5a5a55` subtle inactive rows). No neon glow, no gradients, no drop shadows, no glassmorphism, no blue-black generic SaaS dark mode, no clutter, NO chat window or message thread anywhere. Color is strictly surgical: warm tactile amber `#f0ad28` marks the single item needing human judgment, muted green `#4aba7a` marks pass/landed dots, and muted crimson `#d9534f` appears only on the single clash junction and removed diff line.

Ultra-thin 32px top hardware-inspired status rail separated by a 1px hairline:
- Left: tiny sharp monochrome geometric `A` mark, `Acan`, hairline slash, `acan` repo pill, and two subtle tiny monochrome-ringed teammate initials badges `ND` and `AK` (quiet multiplayer presence).
- Center: subtle recessed dark pill with a single 5px warm amber LED dot: `1 needs you · clash on acan-core`.
- Right: muted monospace `Droid · synced` with tiny green dot, and `⌘K`.

Three-bay architectural layout with tight native spacing and razor-sharp 1px dividers (zero wasted gaps, zero heavy nested boxes):

1. Left Bay (24% width, `#1c1c1a` matte panel) — Quiet Text Order Board:
   - Tiny tracked uppercase micro-header `ORDERS` (9px muted monospace).
   - Five tight, calm, single-line native rows (12px Inter, quiet low-contrast grey until active):
     - Active selected row (subtle `#242421` matte fill + razor-thin `2px` `#f0ad28` warm amber left edge): `Harden clash settlement rules` / tiny subline `acan-core · Clashing · ND`
     - Quiet row 2 (`#8c8c86`): `Wire scope hook into worktree` / `acan-git · Building · AK`
     - Quiet row 3 (`#8c8c86`): `Emit deviations-first receipt` / `acan-intent · Gating · ND`
     - Quiet row 4 (`#666661`): `Scan crate symbol graph` / `acan-scan · Landed` (tiny muted green dot)
     - Quiet row 5 (`#666661`): `CLI session #14` / `read-only` (subtle dashed dot)
   - Pinned cleanly at the bottom of the left bay: one ultra-quiet single-line intent trigger `+ New order...` (single line only, not a chat box).

2. Center Bay (44% width, `#161615` deep matte obsidian living spatial canvas):
   - Tiny top-left engraved micro-label `LIVE SCOPE · acan` and bottom-left tiny quiet legend (`actual`, `declared`, `interlock`).
   - An iconic, serene, living 2D architectural transit schematic of the Rust workspace drawn with razor-sharp precision on an ultra-faint dark dot grid (barely visible `#222220`).
   - Five minimal flat tactile station modules rendered as crisp matte `#1f1f1d` precision rectangles with `1px` `#353531` borders and clean 11px IBM Plex Mono labels: `acan-scan`, `acan-git`, `acan-core`, `acan-intent`, `acan-server`, connected by crisp `1px` orthogonal and 45-degree matte belt lines (`#3a3a36`).
   - Living agent activity with zero visual noise:
     - A crisp solid soft-ivory active path line runs from `acan-scan` into `acan-core`, with one tiny subtle muted-teal agent dot `w1` steadily working near `acan-git` with a faint short trailing wake.
     - A fine dashed steel-grey declared-scope path from `acan-intent` tries to enter `acan-core`, where one tiny warm-amber-ringed agent dot `w2` is cleanly held behind a sharp minimal horizontal amber barrier tick mark labeled in tiny 10px mono `held · clash.rs`.
   - Huge breathing room around the schematic so the eye immediately rests on the single amber hold gate without effort.

3. Right Bay (32% width, `#1c1c1a` matte inspector panel) — Generative Flat Evidence Blocks & Tactile Settlement Controls:
   - Separated cleanly by `1px` `#2e2e2b` horizontal hairlines (zero stacked floating cards):
   - Top block (`CLASH · T-04 × T-07`): crisp 13px Inter Medium headline `Both tasks declare clash.rs` and one calm secondary line `T-07 held before write. Pick settlement.`
   - Middle block (`DIFF · crates/acan-core/src/clash.rs`): authentic compact 11px IBM Plex Mono syntax-highlighted Rust code diff inside a recessed `#141413` code well with subtle muted green/red line markers:
     ```
     pub enum Settlement {
         Narrow { task: TaskId },
     +   Serialize { first: TaskId, then: TaskId },
         SplitAtContract { owner: TaskId, contract: String },
     }
     ```
   - Third block (`RECEIPT · VERIFIED`): ultra-compact 3-column flat hardware-style telemetry strip in 11px mono: `SCOPE enforced` · `TESTS 42 pass` · `DEVIATIONS 0` (tiny muted green indicator dots).
   - Bottom block (`SETTLEMENT`): three flat Dieter Rams / Teenage Engineering tactile matte keycap action buttons stacked cleanly with square monospace keycaps on the left:
     - Suggested primary button (`#262520` matte surface, `1px` warm amber `#f0ad28` border, `#f0ad28` amber keycap `1`, soft-ivory text): `1   Serialize T-04 then T-07`
     - Secondary matte button (`#21211f` surface, `1px` `#333330` border): `2   Narrow T-07 scope`
     - Secondary matte button (`#21211f` surface, `1px` `#333330` border): `3   Split at contract`

Razor-sharp native Retina rendering, crystal-clear Inter and IBM Plex Mono typography, zero typos, zero extra chrome, calm dark studio hardware-grade craft that feels unmistakably innovative, fast, and effortless on the eyes.
