# Day 1 Acan V1 UI Mockup Prompts

Use these with GMI image generation (`gpt-image-2-generate`, `reve-2-1`, `flux-kontext-pro`) only after `get_model` and `estimate_generation`, with human approval before `submit_generation`. The model assigned to each direction is the planned choice. Confirm it with `get_model` at run time.

## Shared constraints (add to every direction)

- 16:9 widescreen desktop application screenshot.
- Native desktop and web egui style: immediate-mode widgets, crisp 1px borders, compact pills, high legibility, low visual bloat. Not glossy, no glassmorphism, no cluttered template look.
- NO chat window, NO chat sidebar, NO message input box, NO send button anywhere in the frame.
- The main screen is a clean text board of orders. Each order shows intent, scope, and checks.
- Realistic developer labels only. No lorem ipsum. All text legible and spelled correctly.

## Direction A: Crisp Technical Light (Swiss Transit / CAD)

A 16:9 widescreen screenshot of a native desktop developer tool called Acan, rendered in an immediate-mode egui style. Warm off-white drafting-paper canvas with a faint grid. Sharp 1px charcoal borders on every panel, no shadows, no rounded glass effects. Three-column layout.

Left column: an Order Board titled "Orders" listing three text rows, each with a short intent line, a scope label, and a status pill: "Approved" (muted green pill), "Held: Interlock" (amber pill), "Receipt Ready" (charcoal outline pill).

Center: a transit-style 2D subway-line map of one Rust repository, with station nodes labeled "crates/core", "crates/server", "crates/git", and "crates/scan". A dotted line shows the planned path, a solid charcoal line shows the actual trail, and one highlighted interlock node sits where two lines clash, marked with a small amber hold symbol.

Right column: a compact Approval and Receipt card with a verdict line, a short diff summary, and two explicit buttons labeled "Approve Scope" and "Bounce".

No chat sidebar, no message box, no input field anywhere. Crisp sans-serif for labels, monospace for paths and IDs. Clean, high-legibility, dense but uncluttered.

## Direction B: Dark Instrument Panel (egui Industrial / Terminal-Native)

A 16:9 widescreen screenshot of a native desktop developer tool called Acan in a dark instrument-panel style, inspired by precision avionics displays and native egui tools. Deep matte charcoal-slate background with a muted fine grid. Crisp monospace headers. Thin 1px light-gray borders, compact rectangular status pills, no bloom and no neon.

Left column: an Order Board with three text order rows showing intent, scope, and check lines.

Center: a transit-style 2D repository topology drawn as clean line segments and station dots. Two agent lines in muted tones (one teal, one slate-blue) run across the map. One amber held-interlock gate, drawn as a small square barrier symbol, blocks one junction. Glow is limited to the amber gate only.

Right column: an anchored Receipt and Scope Diff card with a file list in monospace and deterministic check badges. Two rows show "PASS" and one row shows "BOUNCED".

No chat sidebar, no message input, no send button anywhere. Dense, legible, precise.

## Direction C: High-Density Split Dispatch Desk

A 16:9 widescreen screenshot of a native desktop developer tool called Acan with an ultra-clean utilitarian layout. Cool light-gray chrome, high-contrast near-black ink text, white panel surfaces with 1px gray dividers, no decorative gradients.

Compact top status bar showing the active repository name "example-repo" and a worker count "Workers: 3".

Main area split into two panes.
- Left pane: expandable Order cards. Each card has a title, a scope path list in monospace, and small check chips ("Check: PASS", "Check: PENDING").
- Right pane: a crisp, minimalist 2D transit-style scope-picker map with toggleable module nodes (some filled, some outlined) connected by a few lines.

Pinned bottom Receipt review bar with a "Review Receipt" label, a verdict chip, and two buttons, "Approve Scope" and "Bounce".

No chat sidebar, no message box, no input field anywhere. Dense, legible, high-contrast.

## Refinement edit template 1: Edit Pass 1 - Layout & Density Cleanup

Use with `upload_media` (3-step flow per its schema) to upload the chosen Direction mockup, then run the image-edit model with this prompt.

Edit the attached Acan desktop UI screenshot. Keep the same overall layout, colors, and panel structure. Layout and density cleanup only:
1. Align all left-column order rows to one consistent vertical rhythm with equal padding.
2. Reduce any gap between panels to a consistent 8 px grid. Remove gaps larger than 16 px.
3. Keep the transit map in the center column with no overlapping labels.
4. Keep the Approval and Receipt card anchored to the right edge.
5. Do not add a chat sidebar, message box, or send button. Do not change any label text.
Output a 16:9 image at the same resolution as the input.

## Refinement edit template 2: Edit Pass 2 - High-Contrast States & egui Fidelity

Run after Edit Pass 1. Upload the Pass 1 output with `upload_media` if the edit model needs a fresh file reference.

Edit the attached Acan desktop UI screenshot. Keep the layout fixed. Changes:
1. Make status pills high contrast: "Approved" dark text on a light green-gray fill; "Held: Interlock" dark text on an amber fill; "Receipt Ready" ink outline with ink text.
2. Make the held interlock node unmistakable with a 2 px amber outline.
3. Make the PASS and BOUNCED check badges readable at a glance with solid fills.
4. Give the "Approve Scope" and "Bounce" buttons a flat egui-style look: 1 px border, no gradient, no shadow.
5. Keep all text legible at 100% zoom. Add no decorative effects. Do not add a chat sidebar, input box, or send button.
Output a 16:9 image at the same resolution as the input.
