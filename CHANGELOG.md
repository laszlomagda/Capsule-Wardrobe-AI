# Changelog

All notable changes to the Capsule Wardrobe Builder will be documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] — 2026-05-09

### Added
- **User Mode Detection** — agent now reads which of five user archetypes is in front of it (Explorer, Expert, Pragmatist, Constrained, Adaptive Shopper) and routes accordingly. Runs before Step 1.
- **Step 1 fallbacks** — explicit paths when the user can't name a style reference or gives concepts instead of people.
- **Diverse style tension examples** — examples now span women, men, subtle/minimal, and functional/practical aesthetics, in both the skill body and `reference_style_tension.md`.
- **Quick Capsule Mode** — compressed 5-step protocol for time-constrained or aesthetics-indifferent users. Delivers 4–5 formulas immediately with the option to deepen later.
- **Confirmation Checkpoints** — explicit confirmation gates before Steps 5, 10, and 11 to prevent building on weak assumptions.
- **Maintaining Progress** snapshot — running summary template that survives long sessions and multi-session breaks.
- **Detecting Structural Constraints** — Step 2 distinguishes preferences from structural constraints (sizing beyond standard range, extreme budget, workplace uniform/regulation, physical accessibility) and instructs the agent to restructure the process around them.
- **For Opportunistic Shoppers** — parallel track for find-then-curate shoppers, including a wildcard allocation and a found-piece decision tree.
- **Cross-reference checkpoints** at Steps 5, 8, and 10 — verify formulas, lifestyle strategy, and shopping list against the constraints from Step 2.
- **Tool-agnostic visual guidance** — colour analysis and outfit visualisation now work with any image-capable AI, with text-only fallbacks if no visual tool is available.
- **`claude-version/SKILL.md`** — readable, version-controlled source committed alongside the packaged `.skill`.

### Changed
- **Inclusive description** — frontmatter description now reads "guides anyone (regardless of gender, budget, or shopping style)".
- **Two-AI section** in the Claude version replaced by tool-agnostic Visual Tools guidance. ChatGPT-specific DALL·E flows are preserved in the ChatGPT version.
- **EXECUTION LOOP** (ChatGPT version) gains a user-mode identification step and a checkpoint-due check.
- **STEP TRANSITION RULE** (ChatGPT version) now references the explicit Checkpoints section.
- **SELF-CHECK** (ChatGPT version) adds the visible-surface uniform-overlay validation to its high-stakes pass.

### Why
This release is grounded in a structured 9-persona test (4 generic adversarial + 5 character personas) that scored v1.1.0 between 2/10 and 5.5/10 on the character walkthroughs. The findings (Miranda Priestly: no expert pathway; The Engineer: assumes enthusiasm; The Curvy Girl: sizing as peripheral; The Closeted PO: no taste/budget reality check; The Factory Worker: plan→buy assumption breaks for opportunistic shoppers) drove the eight rewrites that became this release.

## [1.1.0] — 2026-04-15

### Added
- ChatGPT version packaged as a standalone folder, with Custom GPT setup instructions
- `SYSTEM_INSTRUCTIONS.md` for use as the system prompt of a ChatGPT Custom GPT
- Three reference files for ChatGPT knowledge base (`reference_style_tension.md`, `reference_palette_example.md`, `reference_formula_template.md`)
- YAML frontmatter on all reference files for machine-readable metadata
- Repo restructured into `claude-version/` and `chatgpt-version/` folders for clearer audience separation
- Local `README.md` in each version folder for subfolder navigation

### Improved (agent-design refinements)
- Added **execution loop** to both Claude and ChatGPT versions — internal validation before responding
- Added **step transition rule** — prevents premature movement between steps, especially rushing Step 1
- Added **self-check** for high-stakes outputs (final formulas, palettes, shopping lists)
- ChatGPT version: added **operating hierarchy** block to enforce file priority
- ChatGPT version: added **reference triggers** specifying when to consult each reference file
- Expanded guidance on body data collection (size, height, shape) for accurate DALL·E outfit rendering
- Expanded guidance on uniform constraints (doctor's coat, airline uniform, etc.) and how they reshape the visible outfit canvas
- Expanded palette step to require visual swatches, not just colour names

### Fixed
- Colour palette step no longer implies the user's closet reveals what suits them — palette now properly derived from colour analysis, cross-checked with uniform constraints, and filtered by desire
- Skill now asks for existing colour analysis first before running its own

## [1.0.0] — 2026-04-14

### Added
- Initial release of the Capsule Wardrobe Builder skill
- 11-step guided process for building a personalised capsule wardrobe
- Two-AI workflow integration (Claude for analysis and systems, ChatGPT for visual rendering and colour analysis)
- Style reading methodology for analysing reference people and outfits
- Style tension framework for articulating personal style identity
- Outfit formula structure (8–12 formulas with sub-variations)
- Shopping list prioritisation logic
- Claude Project setup guide (non-technical version for sharing)

### Package contents
- `capsule-wardrobe-builder.skill` — installable skill file for Claude Cowork and Claude Code
- `Claude_Project_Setup_Capsule_Wardrobe_Builder.md` — copy-paste instructions for setting up a Claude Project
- `README.md` — project overview and installation instructions
