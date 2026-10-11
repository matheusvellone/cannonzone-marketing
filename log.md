# Log

Newest at the bottom. One entry per action or measurement.

## 2026-09-25

- v1 of the game shipped.

## 2026-10-01

- Posted link posts to r/playmygame and r/WebGames at the same time, titled "Cannonzone: physics-based puzzle cannon shooter". **0 interactions** on both. Diagnosis is in `strategy.md`.
- Decided on a video-first approach: short clips of levels built for video, each with its own play link, compared against each other.
- Built 3 showcase levels with the `/new-level` skill: Trick Shot, Barrel Blast, Hidden Route. All pass the Publish checks. (The level simulator gained rotating-cannon support to make Barrel Blast.)
- The user published all three as community levels; they were approved the same day:
  - Trick Shot: `QPOW-LJLY-AEDZ`
  - Barrel Blast: `HHRP-WJTV-QFQM`
  - Hidden Route: `GISE-SQZW-LMZG`
- Recorded 6 clips (3 levels × vertical and landscape) with a frame-by-frame replay recorder. It became the `/record` skill in the game repo. The silent clips are in the game repo's `tmp/videos/` (not stored here).

## 2026-10-02

- Created this repo and consolidated the strategy, the experiment and the drafts here. Media isn't stored: levels live in the production database, and clips get re-rendered or downloaded from the posts.
- Next: add sound, post Barrel Blast first (see `experiments/2026-10-showcase-levels.md`), then log the results here.

## 2026-10-11

- Since the last entry the game gained checkpoint cannons, achievements, death markers and trajectories, fillable walls, a main menu built around community levels, music, and a death heatmap for level analytics. The 3 showcase clips were never posted.
- Reviewed the old clips: in vertical, the level only filled the middle of the frame, so the ball and cannons were a few pixels on a phone. The camera never moved.
- `/record` gained a director camera: it opens on the whole level, pushes in 1.7× to follow the ball in vertical (`--zoom`), and pulls back out to the whole level on the win. Soft scrims sit behind the caption and footer. Landscape is unchanged.
- The showcase levels' local files were gone from the game repo's `tmp/levels/`, and production still rejects the `.env` `ADMIN_TOKEN` (401). The user pasted Barrel Blast's JSON; its winning shots (with the coin, 8.6 s of play) were rebuilt with the level simulator and replay as a full clear.
- Re-rendered `barrel-blast-vertical.mp4` and `barrel-blast-landscape.mp4` (13.9 s, with music and sound effects) into the game repo's `tmp/videos/`.
- Next: post Barrel Blast to r/IndieGaming as a native video, with the link in the first comment. Then #screenshotsaturday on 2026-10-17 and an itch.io upload.
- Posted Barrel Blast to r/IndieGaming as a native video (the vertical clip) by u/Spykman: "I'm developing a browser game where you are the cannonball". The body text is the user's own: the idea dates from college, a few weekends of work, a level editor inspired by Super Mario Maker, and the play link `https://cannonzone.com/?code=HHRP-WJTV-QFQM`. The link is a text link whose target carries `utm_source=reddit&utm_campaign=r-indiegaming`. The user added the GenAI disclosure soon after posting. Post: https://www.reddit.com/r/IndieGaming/comments/1x3j3jz/im_developing_a_browser_game_where_you_are_the/. Results due around 2026-10-13.
- First comment on the r/IndieGaming post: "Seems alright. But you can tell it's vibe coded. Gives Qwen one shot vibes". Read as a reaction to the look (dark navy, cyan glow, system font, stock UI card), which matches the default style of AI-made web games. Suggested a short, non-defensive reply asking what gives it away. Parked "visual identity" in `ideas.md`, waiting on more comments.
