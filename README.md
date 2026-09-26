# itch-theme

Custom theme for my itch.io profile: [zirok.itch.io](https://zirok.itch.io)

itch limits the Custom CSS box to 5120 characters, so the full stylesheet lives here and itch loads it through jsDelivr.

## Setup on itch

**Edit theme**

| Setting | Value |
| --- | --- |
| BG | `#0b0a14` |
| Text | `#f3f1fb` |
| Link | `#4de3f5` |
| Font | Chakra Petch |
| Background | [`stars.png`](stars.png) |

**Custom CSS** (just this line):

```css
@import url(https://cdn.jsdelivr.net/gh/SebasKoria/itch-theme@v2.0.1/zirok.css);
```

**Profile content** (HTML mode): paste [`profile.html`](profile.html).

## Updating

The `@import` points to a tagged version, so nothing gets stuck in a cache.

1. Edit `zirok.css`, commit and push.
2. Tag a new version and push it:
   ```bash
   git tag v2.0.2
   git push origin v2.0.2
   ```
3. On itch, change the version in the `@import` line to the new tag and save the theme.

## Things to update by hand

- The numbers in the scoreboard (`profile.html`) when you publish a game.
- The "Next game loading" card fills the empty slot in the grid. Delete that block in `zirok.css` when a new game fills the row.
- New games get the cyan accent. Add a line with the game's id next to the other per-game colors to give it its own.
