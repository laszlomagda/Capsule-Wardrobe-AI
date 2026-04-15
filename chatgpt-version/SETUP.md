# Setting Up the Capsule Wardrobe Builder in ChatGPT

This folder contains everything you need to run the 11-step capsule wardrobe process in ChatGPT. You have two ways to use it.

## Option A: Create a Custom GPT (recommended)

If you have ChatGPT Plus, this is the cleanest setup — the GPT will guide you through the process without you having to paste anything each time.

1. Go to **chat.openai.com** → click your profile → **My GPTs** → **Create a GPT**
2. Click **Configure** (top tab)
3. **Name:** Capsule Wardrobe Builder
4. **Description:** Guides you through building a personalised capsule wardrobe in 11 steps
5. **Instructions:** Copy the entire content of `SYSTEM_INSTRUCTIONS.md` and paste it here
6. **Knowledge:** Upload these files:
   - `reference_style_tension.md`
   - `reference_palette_example.md`
   - `reference_formula_template.md`
7. **Capabilities:** Keep "Web Browsing" and "DALL·E Image Generation" enabled. DALL·E is essential for Step 6 (outfit visualisation).
8. **Save** — and your GPT is ready to use

You can now open your Custom GPT any time and just say "help me build a capsule wardrobe" to start.

## Option B: Use it as a one-off prompt

If you don't have ChatGPT Plus, you can still use this:

1. Start a new ChatGPT conversation
2. Copy the entire content of `SYSTEM_INSTRUCTIONS.md`
3. Paste it as your first message
4. The assistant will read the instructions and start guiding you through the process

You'll need to re-paste the instructions each new conversation, so Option A is much cleaner for ongoing use.

## What you'll do in the process

The builder walks you through 11 steps, typically across several sessions:

1. Find your style tension (who you admire and why)
2. Share your real-life constraints (schedule, climate, body, budget)
3. Upload reference images (your wardrobe + inspiration)
4. Get your colour palette (seasonal analysis)
5. Build outfit formulas (8-12 complete outfits)
6. Visualise outfits with DALL·E (this step is why ChatGPT shines)
7. Push back and refine
8. Add lifestyle strategy
9. Explore accessories and special pieces
10. Get your shopping list
11. Generate your final documents

## A note on expectations

This is a hypothesis-building process, not a verdict. The best outcomes come from users who push back, correct, and refine. Don't accept any recommendation that doesn't feel like you — the point is to find *your* system, not to follow a formula.

## Related: the Claude version

If you prefer Claude Cowork or Claude Code, there's a packaged skill version of this same process in the `claude-version/` folder of this repo. Install the `.skill` file and it works the same way — the content is identical, just packaged differently for each platform.
