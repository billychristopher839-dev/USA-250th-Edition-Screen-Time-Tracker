# The Republic of Discipline — USA Prosperity Game

A patriotic, USA-themed screen-time habit tracker. You play the Government of the
United States: log your daily screen time, and the less you scroll, the more the
nation prospers. Journey from 1776 to 2026 across 250 days, relive a real piece of
American history each year, and unlock all 50 states.

## How to publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `usa-prosperity`).
2. Upload **everything in this folder**, keeping the structure intact:

   ```
   index.html
   assets/
     eagle.png
     flag.png
     america.mp3
     stars.mp3
     scenery/
       01_sf.jpg ... 14_nasa.jpg
   ```

3. In the repo, go to **Settings -> Pages**.
4. Under "Build and deployment", set **Source = Deploy from a branch**,
   **Branch = main** (or `master`) and **Folder = / (root)**, then **Save**.
5. Wait ~1 minute. Your game will be live at:
   `https://<your-username>.github.io/<repo-name>/`

That's it. The game saves progress in your browser (localStorage), so each visitor
keeps their own Republic.

## Run it locally

Because the game loads image/audio files, open it through a tiny local server
(double-clicking the file may block the assets in some browsers):

```bash
cd usa-prosperity
python3 -m http.server 8000
# then open http://localhost:8000
```

## Editing the game

- **Nation name, victory length, indicator values:** use the in-app
  "Amendments / Edit" button — no code needed.
- **Swap photos:** replace any file in `assets/scenery/` (keep the same name), or
  edit the `SCENERY` list near the bottom of `index.html` to change captions.
- **Anthems:** replace `assets/america.mp3` / `assets/stars.mp3`.
- **History events:** edit the `EVENTS` object in `index.html` (one positive and
  one negative event per year, 1776-2025).
- **States:** edit the `STATES` array in `index.html`.

## Credits & notes

- Map: "Blank map of the United States" (state paths keyed by postal code).
- Historical event lines are concise, fact-based summaries for educational play.
- Built as a single self-contained `index.html` plus media assets.
