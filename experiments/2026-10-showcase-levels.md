# Experiment: showcase levels (October 2026)

**Question:** Which kind of level makes the best clip, measured by engagement and by people clicking through to play?

**Setup:** We built three levels designed for video (each about 1400×1400 so they crop to both 9:16 and 16:9, all easy-medium so people who click can win). Each one is published as a community level with its own code, so plays can be attributed per post.

| Level | Code | Play link | Concept |
| --- | --- | --- | --- |
| Trick Shot | `QPOW-LJLY-AEDZ` | https://cannonzone.com/?code=QPOW-LJLY-AEDZ | One cannon, one perfect shot that banks off two glowing bouncy walls into a cup on a tower |
| Barrel Blast | `HHRP-WJTV-QFQM` | https://cannonzone.com/?code=HHRP-WJTV-QFQM | DK-style chain: c1 → r1 → r2 → r3 → goal. r2 turns and fires itself on a countdown |
| Hidden Route | `GISE-SQZW-LMZG` | https://cannonzone.com/?code=GISE-SQZW-LMZG | A charge cannon; the red key is hidden in fog that clears as the ball explores; the goal box is behind a red door |

All three were approved on 2026-10-01 with 0 players.

## Level details

- **Trick Shot:**
  - The winning shot is c1 at −50°, and it wins anywhere from −53° to −48.5° (10 angles at 0.5° steps).
  - A rainbow coin sits in the top-right corner above the right wall. Getting it takes a riskier shot at about −59.5°.
  - Edges send the ball back to the start.
- **Barrel Blast:**
  - Route: c1 fires at a locked −60° → r1 fires about 0.58 s after loading → r2 fires itself at −26° → r3 fires about 0.51 s after loading into the goal.
  - Timing windows: about 0.17 s for r1 and about 0.27 s for r3.
  - The coin comes from an early, steep r3 shot.
  - Edges return the ball to the last cannon. A hazard pit sits at the bottom.
- **Hidden Route:**
  - A key lob at −95° (about 87% charge), a coin lob at −82° at full charge, then the final shot at full charge at −74°, which wins at 13 angles.
  - Edges return the ball to the last cannon.

The levels live in the production database. Local copies (`<slug>.json`, `.shots.json` with the verified full clear, `.png` preview) are in the game repo's gitignored `tmp/levels/`.

## Clips

`<slug>-vertical.mp4` (1080×1920) and `<slug>-landscape.mp4` (1920×1080), 60 fps, **silent**, rendered with `/record` into the game repo's `tmp/videos/` (not stored here; re-render or download from the posts). Each clip:

- opens on the whole level with the hook caption, and holds 1.5 s before the first shot
- plays the full clear, coin side trips included
- ends on "Level clear! Play it free → cannonzone.com/?code=…", held for 2.5 s
- shows the footer "Free in your browser · cannonzone.com" throughout

| Level | Caption | Length |
| --- | --- | --- |
| Trick Shot | One shot. Two bounces. Can you find the angle? | 8.4 s |
| Barrel Blast | You ARE the cannonball. | 13.5 s |
| Hidden Route | The key is hidden somewhere in the fog... | 11.8 s |

Before posting, add a sound: a trending sound on TikTok or Shorts, or a light music bed on Reddit.

## Posting plan

- One level per post, 2–3 days apart, each with its own play link in the first comment.
- Change only the clip between posts: same subreddit type, similar time of day.
- Suggested order: Barrel Blast (strongest hook), then Trick Shot, then Hidden Route.
- Drafts are in `../posts.md`.

## Results

Fill in about 48 h after each post. Get Reddit numbers from the user, plays and clears from the community page, and new players from that post's `utm_campaign` (the query in the game repo's `docs/backend.md`, or OneDollarStats).

| Date | Level | Channel / subreddit | utm_campaign | Post link | Upvotes | Comments | Views | New players (utm) | Plays (code) | Clears | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 2026-10-11 | Barrel Blast | r/IndieGaming (vertical clip) | `r-indiegaming` | [post](https://www.reddit.com/r/IndieGaming/comments/1x3j3jz/im_developing_a_browser_game_where_you_are_the/) | | | | | | | First post. Body written by the user |

## What to do with the result

- Make more levels like the winner, and re-cut its clip for the other channels.
- Comments asking for things are the real feature backlog. Add them to `../ideas.md`.
