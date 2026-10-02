# Cannonzone marketing

This repo holds the marketing for **Cannonzone** (https://cannonzone.com): strategy, experiments, post drafts and a dated log. It holds no media: levels live in the production database, and clips can be re-rendered with `/record` or downloaded from wherever they were posted. The game's code lives next door in `../canonzone` (note the single "n" in the folder name).

The game: a free browser physics puzzle game. You are a ball that only moves by being fired from cannons. Grab 3 stars to unlock the goal, then reach it. It has a campaign, a level editor, and **community levels** with share codes (`cannonzone.com/?code=ABCD-EFGH-IJKL`).

## Where things are

| File | What |
| --- | --- |
| `strategy.md` | Why the first posts failed, the channel plan, the hooks, and what not to build yet |
| `experiments/2026-10-showcase-levels.md` | The current experiment: 3 showcase levels, codes, clips, posting plan, results table |
| `posts.md` | Ready-to-paste post drafts per level and channel |
| `log.md` | Dated log of every marketing action and its result. **Append to it** whenever something is posted or measured |
| `ideas.md` | Growth ideas and product ideas that came up, unbuilt, with why they're parked |

## Tools (in the game repo)

Run these from `../canonzone`:

- **`/new-level` skill** (`.claude/skills/new-level/`): designs a level by simulating real shots headlessly, so it's solvable and passes Publish. Writes `tmp/levels/<slug>.json`, `.shots.json`, `.png`. The user pastes the JSON in the editor (**Import ▾ → Paste JSON…**) and publishes it as a community level.
- **`/record` skill** (`.claude/skills/record/`): records a level's clear as silent 60 fps MP4s (1080×1920 and 1920×1080) with a hook caption, footer and play link, into the game repo's `tmp/videos/` (gitignored).
  - **Goal:** `--code` alone fetches the level and its proof of clear from production, so nothing needs to be stored. As of 2026-10-02 that doesn't work yet: production rejected the `.env` `ADMIN_TOKEN` (401). Access is still being worked on.
  - **Until then,** pass `--level` and `--shots` files. For the showcase levels, the game repo's `tmp/levels/<slug>.json` and `.shots.json` are local copies:
  ```sh
  cd ../canonzone && node --env-file-if-exists=.env .claude/skills/record/scripts/record.ts \
    --level tmp/levels/<slug>.json --shots tmp/levels/<slug>.shots.json --code <CODE> --caption "<hook>"
  ```
- **Play stats**: the community page in the game/editor shows players and votes per level, which is how experiments are measured. Plays per level are tracked server-side; there's no referrer or UTM tracking, so **use one share code per post** to attribute traffic.

## Working rules

- **Don't build features before there are players.** The game already has plenty of mechanics. New features should come from what players ask for in comments. See `strategy.md`.
- Reddit can't be read from Claude's tools (fetch and browser are both blocked). Ask the user to paste post stats and comments.
- Never post on the user's behalf. Draft the post; the user posts it.
- Log every post and every measurement in `log.md` with its date, and fill in the experiment's results table.
