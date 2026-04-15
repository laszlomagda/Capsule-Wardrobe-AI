# Changelog

All notable changes to the Capsule Wardrobe Builder will be documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
