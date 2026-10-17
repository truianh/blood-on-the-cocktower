# Blood on the Cocktower

**Clock the Cock. Save the Town.**

A campy, browser-based Townsquare and Storyteller companion for in-person social deduction game nights inspired by *Blood on the Clocktower*. Manage the circle, track the town's fate, run nominations and votes, and give the whole room a theatrical Day/Night experience—complete with custom artwork, sound effects, opening lore, and a dramatic final reveal.

**[Play Blood on the Cocktower](https://truianh.github.io/blood-on-the-cocktower/)**

> **Content note:** This is a playful, adult-humor parody with innuendo and horror-themed imagery. It is an unofficial fan-made companion, not an official *Blood on the Clocktower* product.

## Features

### The Townsquare

- **5–20 players** seated around a circular board, with editable names and swappable seat positions.
- **Traveller support**, with a separate count and distinction between Base players and Travellers.
- **Four custom player states:** **Erect** (alive), **Hot Seat** (facing execution), **Dickmatized** (dead, ghost vote available), and **Drained** (dead, ghost vote spent).
- Player tokens, status stickers, seat numbers, and a legend designed for an across-the-room display.
- Live counts for surviving players and remaining ghost votes, plus a reference table for default role counts.

### Storyteller-led gameplay

- Progress through **Night 0 → Day 1 → Night 1** and subsequent phases using **Next phase** and **Previous**.
- Choose a **nominator** and **nominee**, confirm the nomination, then begin a vote with an illustrated rotating voting pointer.
- Tally votes, record failed votes, move a successful nominee to the **Hot Seat**, and execute the player on the block.
- Track who has already nominated or been accused during the current day and manage spent ghost votes.
- Use separate, configurable **private-chat** and **public-discussion** countdown timers, with pause, reset, and ±10-second controls.

### Private setup and cinematic presentation

- Assign the **original Demon** (required before starting) and optionally the **Mayor** in the private Setup view.
- Reassign the current Demon during Night when required by the game (for example, after an Imp pass or Scarlet Woman takeover).
- Switch to **Present board** for a TV/projector-friendly layout with Day/Night artwork and phase-aware controls. Secret roles are not shown on the public player tokens.
- Begin with a clickable title crest and an illustrated, panel-by-panel **Cocktower Lore** introduction.
- Finish with a two-panel **Good Wins / Evil Wins** cinematic. The ending is selected from the tracked Demon and Mayor state when the Storyteller confirms the game has ended.
- Enjoy event sound effects, page-turn and nomination cues, and persistent **mute/volume** controls.

## How to play

1. **Open the app** using the link above. Click the title crest and proceed through the opening lore to reach Setup.
2. **Prepare the Townsquare.** Set the number of players, enter their names, mark any Travellers, and arrange the seating order.
3. **Set secret roles privately.** Choose the original Demon; select a Mayor if one is in play. Do this before showing the setup screen to the group.
4. **Select Start Game.** The app resets to **Night 0** and enters presentation mode. Advance to **Day 1** when the town wakes.
5. **Run each day.** Select the nominee and nominator, confirm the nomination, start the vote, record the tally, and resolve the Hot Seat or failed vote. Advance through Day and Night as the Storyteller directs.
6. **End the game.** Choose **End Game**, confirm that play has concluded, and reveal the final Good or Evil cinematic.

This is a **Storyteller-operated companion**, not a replacement for a Storyteller. The Storyteller remains responsible for resolving abilities, adjudicating edge cases, and deciding when a game has ended.

## Saving and restoring a game

The app saves supported game state in your browser using `localStorage`, including names, seating, statuses, phases, timer settings, nominations, and secret role assignments. Browser storage **does not synchronize across devices or browsers**.

Use **Export setup** to download `blood-on-the-cocktower-setup.json`, and **Import setup** to restore it later or move it to another device.

> **Keep exported JSON files private.** They can contain hidden Demon/Mayor assignments and other Storyteller-only information. Clearing browser data or using a different browser may also remove locally saved state.

## Run locally

The app uses plain **HTML, CSS, and JavaScript**—no framework, package manager, or build step is required.

1. Download or clone this repository.
2. Keep `index.html` and the complete `Assets/` folder together at the repository root.
3. Open `index.html` in a modern browser, or use a small local web server for more consistent browser behavior:

   ```bash
   python -m http.server 8000
   ```

4. Visit **http://localhost:8000/** in your browser if using the local server.

An internet connection may be needed to load the Google Fonts referenced by the page; local fallbacks are provided.

## Repository structure

```text
blood-on-the-cocktower/
├── index.html                # The complete application
├── Assets/                   # Keep the filenames and capitalization intact
│   ├── cocktower-crest-transparent.png
│   ├── Cocktower-Crest-Transparent.png
│   ├── Day-background.png
│   ├── Night-background.png
│   ├── Center-day.png
│   ├── Center-night.png
│   ├── day-townsquare.png
│   ├── night-townsquare.png
│   ├── opening-cover.jpg
│   ├── opening-1.jpg ... opening-10.jpg
│   ├── ending-neutral.jpg
│   ├── good-win.jpg
│   ├── evil-win.jpg
│   ├── voting_pointer.wav
│   └── ...                   # Additional tokens, stickers, artwork, and audio
└── README.md
```

**Asset paths are case-sensitive on GitHub Pages.** Keep all referenced filenames exactly as written in `index.html`, including the differently capitalized crest filenames. Missing or renamed files can leave backgrounds, tokens, comic panels, or sounds unavailable.

## Publish with GitHub Pages

1. In the repository, open **Settings → Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Select **`main`** and **`/ (root)`**, then click **Save**.
4. Check the **Actions** tab for a successful **pages build and deployment** run.
5. Visit **https://truianh.github.io/blood-on-the-cocktower/**.

Future commits to `main` will trigger another Pages deployment. If an updated site appears unchanged after a successful deployment, try a hard refresh to bypass cached HTML.

A Jekyll theme is not needed for this standalone HTML app.

## Credits and rights

*Blood on the Cocktower* is an unofficial, humor-driven fan companion inspired by *Blood on the Clocktower*. The original game's name and associated rights belong to their respective owners. This project is not affiliated with or endorsed by the original game's creators.

Artwork, audio, fonts, and other third-party materials may be subject to separate licenses or usage terms. **No license to reuse this repository's code or assets is granted by this README**; consult the repository's license information, if provided, and verify rights before redistribution.