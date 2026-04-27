# Reef Runner 🐟

A Pac-Man-inspired game with an underwater theme. You're a hungry little fish navigating a coral reef — eat all the plankton to clear the level, dodge the jellyfish, and grab a glowing pearl to turn the tables and chomp them right back.

## Play

Open `index.html` in any modern browser. No build step, no dependencies.

**Controls**
- Arrow keys or WASD to move
- On mobile: swipe in any direction

**Mechanics**
- Eat all yellow plankton to clear the level
- 4 jellyfish chase you, each with its own personality (chaser, ambusher, wanderer, patroller)
- Glowing pearls let you eat jellyfish for ~7 seconds (200 points each)
- 3 lives — touching a jellyfish without a pearl active costs you one
- Speed ramps up each level

## How to host this on GitHub Pages (free)

GitHub Pages serves any static site at `https://YOUR-USERNAME.github.io/REPO-NAME/`. Full walkthrough:

### 1. Create a GitHub account
Sign up at https://github.com if you don't have one.

### 2. Create a new repository
1. Click the **+** icon top-right → **New repository**
2. Name it `reef-runner` (or whatever you like)
3. Set it to **Public** (Pages requires public repos on free accounts)
4. Don't check any of the "Initialize" boxes — you have files already
5. Click **Create repository**

### 3. Upload the files

**Easiest — drag and drop:**
1. On the new repo page, click **uploading an existing file**
2. Drag `index.html` and `README.md` into the box
3. Scroll down, click **Commit changes**

**Or with git on the command line:**
```bash
cd path/to/reef-runner
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/reef-runner.git
git push -u origin main
```

### 4. Turn on GitHub Pages
1. In your repo, click **Settings** (top tab)
2. Click **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Pick branch **main**, folder **/ (root)**, click **Save**
5. Wait ~30 seconds, refresh — your URL appears in a green box:
   `https://YOUR-USERNAME.github.io/reef-runner/`

That URL works on any device. To update the game, just push new commits — Pages redeploys within a minute.

## Tweaking the game

Everything's in `index.html`. Some quick knobs:

- **Maze layout** — edit the `MAZE` array near the top. `1` = wall, `0` = plankton, `2` = empty, `3` = pearl, `4` = jellyfish spawn
- **Jellyfish speed** — change `1.6 + level * 0.1` in `resetEntities()`
- **Player speed** — change `speed: 2` in the player object
- **Pearl duration** — change `powerTimer = 60 * 7` (60 frames × seconds)
- **Colors** — edit the CSS variables at the top of the `<style>` block
- **Number of jellyfish** — controlled by spawn points (`4`s) in the maze

## Credits
Inspired by Pac-Man (1980, Namco). All art and code here is original — no trademarked names, characters, or assets.

## License
MIT — yours to modify and share.
