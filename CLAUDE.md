# Cannonzone marketing

This repo holds the marketing for **Cannonzone** (https://cannonzone.com): strategy, experiments, post drafts and a dated log. It holds no media: levels live in the production database, and clips can be re-rendered with `/record` or downloaded from wherever they were posted. The game's code lives next door in `../cannonzone`.

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

Run these from `../cannonzone`:

- **`/new-level` skill** (`.claude/skills/new-level/`): designs a level by simulating real shots headlessly, so it's solvable and passes Publish. Writes `tmp/levels/<slug>.json`, `.shots.json`, `.png`. The user pastes the JSON in the editor (**Import ▾ → Paste JSON…**) and publishes it as a community level.
- **`/record` skill** (`.claude/skills/record/`): records a level's clear as 60 fps MP4s (1080×1920 and 1920×1080) with the game's music and sound effects, a hook caption, footer and play link, into the game repo's `tmp/videos/` (gitignored).
  - **Goal:** `--code` alone fetches the level and its proof of clear from production, so nothing needs to be stored. As of 2026-10-11 that still doesn't work: production rejects the `.env` `ADMIN_TOKEN` (401).
  - **Until then,** pass `--level` and `--shots` files. Of the showcase levels, only Barrel Blast has local copies now (the game repo's `tmp/levels/barrel-blast.json` and `.shots.json`); for the others, ask the user for the level's JSON (editor **Export**) and rebuild the shots with `/new-level`'s simulator:
  ```sh
  cd ../cannonzone && node --env-file-if-exists=.env .claude/skills/record/scripts/record.ts \
    --level tmp/levels/<slug>.json --shots tmp/levels/<slug>.shots.json --code <CODE> --caption "<hook>"
  ```
- **Play stats**: the community page in the game/editor shows players and votes per level. Plays per level are tracked server-side.
- **Channel tracking**: the game reads `utm_source` (or `ref`) and `utm_campaign` on a player's first visit, plus the referring site, and stores them on the guest profile (`players.source` / `campaign` / `referrer`). OneDollarStats (onedollarstats.com) counts visits by the same tags. Other UTM parameters are ignored. The players-by-channel SQL query is in the game repo's `docs/backend.md` ("Channels").
  - **Every link you post gets tags**, one `utm_campaign` per post: `https://cannonzone.com/?code=<CODE>&utm_source=reddit&utm_campaign=r-indiegaming`. Sources: `reddit`, `bluesky`, `x`, `tiktok`, `youtube`, `itch`, `hn`. Campaign: the subreddit (`r-webgames`) or the post (`screenshotsaturday-2026-10-17`). Values are lowercased and cut to `[a-z0-9._~-]`.
  - Still give each post its own level code where you can: the level's plays and clears show what happened after people clicked.

## Working rules

- **Don't build features before there are players.** The game already has plenty of mechanics. New features should come from what players ask for in comments. See `strategy.md`.
- Reddit can't be read from Claude's tools (fetch and browser are both blocked). Ask the user to paste post stats and comments.
- Never post on the user's behalf. Draft the post; the user posts it.
- Many subreddits require declaring GenAI use (r/IndieGaming does). Claude helped with the code, the level design and the clips, so every draft carries a short disclosure. Check each subreddit's rules before suggesting it.
- Log every post and every measurement in `log.md` with its date, and fill in the experiment's results table.
