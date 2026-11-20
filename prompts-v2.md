# Acan V1 UI Mockups — Bespoke Art-Directed Prompts (v2)

Designed around Acan's real product aesthetic: calm editorial light software (Linear + Things 3 + Vignelli Swiss transit restraint), pure neutral light surfaces (`#f2f2ef` canvas, `#ffffff` cards, `1px` `#e5e5e2` hairlines, `#18181a` ink, `#8c8c90` muted text), extreme whitespace (~50 to 65 words total on screen), monochrome until human attention is needed, colour strictly for status (`#e1a43c` waiting amber, `#30a46c` pass, `#e5484d` deviation), Inter sans + IBM Plex Mono paths and keyboard shortcut keycaps, zero chat box.

## Prompt 1: Main Screen — Calm Order Board + Anchored Approval Card

Ultra-clean, modern native macOS desktop application UI screenshot (16:9 widescreen) for a minimalist developer tool called Acan. Aesthetic inspired by Linear, Things 3, and Swiss editorial typography: museum-grade restraint, massive breathing room, razor-sharp crisp rendering, flat pure light neutral palette. Background canvas is soft neutral off-white `#f2f2ef`; primary card surface is pure crisp white `#ffffff` with subtle `1px` `#e5e5e2` hairline borders and zero heavy drop shadows. No warm yellow paper, no gridlines, no dark panels, no glassmorphism, no chat sidebar, no message input box anywhere.

Thin minimal top bar (36px tall): left shows a tiny monochrome geometric mark and "Acan" in medium Inter `#18181a` beside a subtle muted pill "All repos"; right shows a quiet monospace shortcut hint "⌘K" and a tiny subtle green dot "Local". Nothing else in the top bar.

Spacious asymmetric two-pane layout with generous 24px outer margins and wide whitespace:

Left pane (58% width): A quiet, airy vertical Order Board with generous vertical spacing between 5 single-line order rows. Four rows are intentionally calm, low-contrast neutral grey (`#57575a` and `#8c8c90`) showing only a crisp intent title, a tiny muted monospace repo tag, and a quiet status word:
- "Add rate-limit middleware to auth router" · `api-gateway` · Running
- "Migrate session store to SQLite WAL" · `core-db` · Running
- "Extract CSV exporter into streaming worker" · `billing` · Landed
- "Normalize webhook retry backoff" · `notify` · Landed

One active selected row sits cleanly in a crisp `#ffffff` row highlight with a subtle 3px warm amber `#e1a43c` left edge bar and dark `#18181a` text:
- "Guard concurrent writes in checkout ledger" · `ledger` · Needs approval (small soft amber `#e1a43c` status dot)

Right pane (38% width): One elevated pure white `#ffffff` Anchored Approval Card with `1px` `#e5e5e2` border, 12px subtle corner radius, and generous 24px padding. Inside the card, clean editorial hierarchy with plenty of whitespace:
- Top: tiny muted monospace label `ORDER 04 · ledger` and warm amber status pill `Needs approval`. Headline in Inter Medium `#18181a`: "Guard concurrent writes in checkout ledger".
- Subtle divider, followed by a calm structured evidence section tagged in tiny muted text `Drafted scope`:
  - Three clean checked monospace file paths with crisp checkboxes: `src/ledger/lock.rs`, `src/ledger/write.rs`, `tests/concurrent.rs`
  - Two minimal inline check pills with tiny green dots: `cargo test` and `clippy`
- Bottom fixed keyboard action bar separated by a hairline border: three crisp flat buttons with clean monospace keycaps inside them:
  - Solid dark ink `#18181a` primary button with white text: `1  Approve scope`
  - Clean white hairline button: `2  Send back`
  - Clean white hairline button: `3  Hold`

Every single word is sharply rendered in Inter and IBM Plex Mono with zero typos, zero extra chrome, zero clutter, and roughly 55 words total across the entire screen.

## Prompt 2: Minimal 45-Degree Swiss Transit Repo Map + Interlock Card

Ultra-clean, modern native macOS desktop application UI screenshot (16:9 widescreen) for a minimalist developer tool called Acan, showing its signature 2D repository map view. Aesthetic inspired by Massimo Vignelli's iconic Swiss transit diagrams fused with Linear's ultra-clean light desktop craft: pure calm `#f7f7f5` light canvas, razor-sharp crisp vector geometry, generous negative space, zero gradients, zero glow, zero 3D, zero chat window, zero message box.

Thin minimal top bar (36px tall): left shows "Acan / ledger" with a subtle segmented view switch showing `Board` (muted) and `Map` (active crisp white pill); right shows `⌘K`.

Main canvas (full-bleed `#f7f7f5` with huge open breathing room): A serene, mathematically crisp 2D schematic transit map of a codebase drawn strictly with horizontal, vertical, and 45-degree diagonal lines (`2px` stroke). About 14 minimal circular station nodes sit cleanly along the tracks. Most untouched stations remain quiet unlabelled hollow light-grey circles (`#c8c8c4`) so the diagram stays effortlessly uncluttered.

Two clean routes cross the diagram:
- A crisp dashed dark-grey line (`#8c8c90`) showing the planned scope route across 3 stations.
- A solid crisp dark ink line (`#18181a`, `2.5px`) showing the agent's actual path.
Only 4 relevant stations carry crisp small IBM Plex Mono labels placed cleanly with zero overlap: `ledger/lock.rs`, `ledger/write.rs`, `ledger/journal.rs`, and `tests/concurrent.rs`.

At the single junction where two lines meet, one unmistakable yet refined warm amber `#e1a43c` circular interlock ring highlights the station, paired with a crisp compact pill right beside it: `Interlock · held`.

Floating cleanly on the right side (340px wide, 24px margin from right edge) is one crisp `#ffffff` hairline card (`1px` `#e5e5e2` border, 12px radius, generous 20px padding) titled `Interlock held`:
- Concise 2-line plain-English note in Inter `#57575a`: "Order 05 wants `ledger/lock.rs` while Order 04 holds active scope."
- Tiny clean legend row showing solid line `Actual`, dashed line `Planned`, amber ring `Interlock`.
- Bottom fixed keyboard buttons: `[1] Hold Order 05` (solid `#18181a` ink fill, white text) and `[2] Inspect scope` (white hairline button).

Under 50 words total across the whole UI. Museum-grade Swiss graphic design clarity, crystal-sharp Inter and IBM Plex Mono typography, zero typos, zero extra toolbars or meters.

## Prompt 3: Deviations-First Receipt & Scope Review Screen

Ultra-clean, modern native macOS desktop application UI screenshot (16:9 widescreen) for a minimalist developer tool called Acan, showing a calm, editorial Receipt review screen after a coding agent finishes an order. Aesthetic inspired by Linear and Stripe Docs craftsmanship on a pure light neutral palette (`#f2f2ef` outer canvas, `#ffffff` crisp cards, `1px` `#e5e5e2` hairline borders, `#18181a` ink, `#57575a` secondary text, `#8c8c90` muted text). Zero chat window, zero message input, zero clutter, zero heavy shadows, zero decorative gradients.

Thin minimal top bar (36px tall): left shows `← Board` beside `Order 04 · Receipt`; right shows a muted monospace commit badge `a91c4e2` and `⌘K`.

Centered, spacious two-column editorial layout (max-width centered with generous margins on both sides):

Left main column (62% width): One pure white `#ffffff` Receipt sheet with `1px` `#e5e5e2` border and generous 28px padding:
- Headline in Inter Semibold `#18181a`: "Guard concurrent writes in checkout ledger"
- Right below the headline, a crisp, understated **Deviations First** callout box with a very soft pale-rose tint (`#fdf5f5`) and a thin `#e5484d` left accent border:
  - Small muted red label: `1 deviation · blocked from landing`
  - Clean line: `config/timeouts.toml` modified outside approved scope (reverted automatically)
- Below a clean hairline divider, section `Approved scope · 3 files`:
  - `src/ledger/lock.rs`  `+64  -12` (muted green/red monospace diff counts aligned right)
  - `src/ledger/write.rs`  `+38  -9`
  - `tests/concurrent.rs`  `+81  -0`
- Bottom fixed keyboard action bar: `[1] Land commit` (solid `#18181a` ink button, white text), `[2] Send back` (clean hairline button), `[3] Open diff` (clean hairline button).

Right secondary rail (32% width): One quiet `#ffffff` hairline card titled `Checks verified` with generous spacing:
- Three crisp rows with small `#30a46c` green dots and right-aligned `Pass`:
  - `cargo test` · `42 passed`
  - `cargo clippy` · `0 warnings`
  - `scope hook` · `enforced`
- Subtle muted footer line: `Nothing outside approved scope can land.`

Ultra-clean modern product design, generous whitespace, crystal-clear Inter and IBM Plex Mono typography, zero typos, ~60 words total across the entire screen.
