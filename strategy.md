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
   - Each post gets its own community level code, which shows its plays and clears.
   - Make sure the first 30 seconds hook a stranger.
   - Make sure the game works well on phones, since most Reddit traffic is mobile.

## Don't fall into the feature trap

There's a pull to "add everything to the game" before there are players. Don't. The game already has 3 cannon types, countdowns, bouncy and hazard walls, fog, keys and doors, and community levels with share links. That's more than enough for good clips. Ship content, measure, and let player comments decide the next feature.

Example: the backlog item that fits the barrel-blast hook best is **"Canhão se movendo"** (moving cannon). It wasn't built, because a rotating cannon with `lockFire` and a countdown already gives the auto-firing barrel feel (see the Barrel Blast level).
