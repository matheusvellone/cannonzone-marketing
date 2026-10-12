# Strategy

## Where we started (2026-10-01)

The game's v1 shipped on 2026-09-25. The first two posts were link posts made at the same time:

- r/playmygame: https://www.reddit.com/r/playmygame/comments/1wuwcwh/cannonzone_physicsbased_puzzle_cannon_shooter/
- r/WebGames: https://www.reddit.com/r/WebGames/comments/1wuwbgj/cannonzone_physicsbased_puzzle_cannon_shooter/

Title: "Cannonzone: physics-based puzzle cannon shooter". Result: **0 interactions** on both.

### Likely reasons

We couldn't open the posts, so these come from how those subreddits work:

1. **They may have been auto-filtered.** A new or low-karma account, a link to a new domain, and the same link in two subreddits at once (the post IDs are consecutive) all look like spam. Check logged out or in a private window whether they show up in each subreddit's "New" tab; if not, message the moderators.
2. **Those subreddits move fast.** "Play my game" posts sink within minutes, and most get zero comments. One post there tells you almost nothing about the game.
3. **The title names a genre, not a hook.** "Physics-based puzzle cannon shooter" fits hundreds of games.
4. **A link post only shows a static thumbnail.** Games get traction on Reddit through a short video or GIF that plays in the feed.

## The plan

1. **Lead with a 10–15 s clip**, and nothing but the satisfying moment: a chain of shots, a near miss, a clever bank. No menus, and it should loop. Post the video natively and put the link in the first comment.
2. **Use a hook people get instantly:**
   - "You ARE the cannonball."
   - "Donkey Kong barrel blasts as a puzzle game", since DK barrel cannons are the closest reference most people know.
   - "Can you find the angle?", which invites comments.
3. **Subreddits:** r/IndieGaming, r/indiegames, r/IndieDev, r/gamedev (Screenshot Saturday thread), r/WebGames (as a video), r/puzzlevideogames, r/playmygame.
   - Read each one's self-promotion rules first.
   - Space posts a few days apart, never two at once.
   - Reply to every comment quickly.
4. **Browser game portals, where players already look:**
   - **itch.io:** upload the HTML5 build; it has real discovery for new browser games.
   - **Newgrounds.**
   - **CrazyGames / Poki:** they curate, but one acceptance beats any number of Reddit posts.
5. **Show HN on Hacker News:** a browser game with a level editor and community levels fits it.
6. **Short-form video:** TikTok, YouTube Shorts and Reels with the vertical clips, plus Bluesky/X with #screenshotsaturday. "Can you solve this level?" is the format.
7. **Give before asking:** play and comment on other people's games in r/playmygame. Many reciprocate, and it builds the karma that keeps posts from being filtered.
8. **Measure:**
   - Each post's link carries UTM tags (`utm_source`, and its own `utm_campaign`), which show where players came from. See `CLAUDE.md`.
   - Each post also gets its own community level code where possible, which shows its plays and clears.
   - Make sure the first 30 seconds hook a stranger.
   - Make sure the game works well on phones, since most Reddit traffic is mobile.

## Don't fall into the feature trap

There's a pull to "add everything to the game" before there are players. Don't. The game already has 3 cannon types, countdowns, bouncy and hazard walls, fog, keys and doors, and community levels with share links. That's more than enough for good clips. Ship content, measure, and let player comments decide the next feature.

Example: the backlog item that fits the barrel-blast hook best is **"Canhão se movendo"** (moving cannon). It wasn't built, because a rotating cannon with `lockFire` and a countdown already gives the auto-firing barrel feel (see the Barrel Blast level).

## Community cold start (2026-10-12)

Community levels need players, and players need good levels. This is a cold start, not a deadlock: the game works with zero community (the campaign, plus `/new-level` turning out solvable levels in minutes). Mario Maker and Geometry Dash launched the same way; official levels carried them, and creators came later, from among the players.

1. **Market the game, not the community.** Nobody joins an empty level-sharing platform; people do play a fun puzzle. Every post sells playing.
2. **Be the first creator, on purpose.** Publish a few good community levels a week with `/new-level`, so whatever a new player opens is worth playing. This is the start of a daily level (see `ideas.md`): curated by us now, pulled from the community later.
3. **Makers come from players, and they're few.** Usually around 1–5% of players ever open an editor, so makers won't show up by themselves until there are hundreds of players. Track the share of players who open the editor and the share who publish (may need tracking in the game).
4. **Pay the first makers in players.** When anyone publishes a decent level, record it with `/record`, post it with their credit and code, and feature it in the menu. "200 people played your level" is what makes a maker build another one and bring friends.
5. **Don't make the community look empty.** A menu of levels showing "0 players · 0 votes" reads as a dead game. Until the numbers are real, lead with the campaign and featured levels, and hide counts below a threshold. This is presentation, not a mechanic, so it's an allowed exception to the feature trap below.
6. **Recruit makers later, where they already are.** Once there are a few hundred players: r/MarioMaker, Geometry Dash and level-design communities, with a small contest whose prize is a featured clip and the daily level. Not before step 4 has some proof.

Order: now we supply the levels and the marketing is about playing → spotlight every early maker → contests and a daily level pulled from the community.
