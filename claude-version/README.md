# Claude Version

This folder contains everything you need to run the Capsule Wardrobe Builder in Claude — whether you use Claude Cowork, Claude Code, or claude.ai.

## Files in this folder

- **`capsule-wardrobe-builder.skill`** — The installable skill file. Drop it into Claude Cowork or Claude Code to add the skill to your library.
- **`Claude_Project_Setup_Capsule_Wardrobe_Builder.md`** — Copy-paste instructions for setting up a Claude Project on claude.ai. Use this if you don't have Cowork or Claude Code.

## Option A: Install as a Skill (Claude Cowork or Claude Code)

1. Download `capsule-wardrobe-builder.skill`
2. **Claude Cowork:** Open the file in Cowork — it will be added to your available skills automatically
3. **Claude Code:** Drop the contents into `~/.claude/skills/capsule-wardrobe-builder/` and the skill will be detected on the next session
4. Start a new conversation and say something like "help me build a capsule wardrobe" — the skill triggers automatically

## Option B: Set up a Claude Project (claude.ai)

1. Open `Claude_Project_Setup_Capsule_Wardrobe_Builder.md`
2. Follow the instructions to create a new Claude Project with the custom instructions pasted in
3. Start chatting with the project — the agent will guide you through the 11-step process

## Looking for the ChatGPT version?

It's in [`../chatgpt-version/`](../chatgpt-version/) — same 11-step process, packaged for ChatGPT Custom GPTs.

## License

MIT — see [../LICENSE](../LICENSE) in the repo root.
