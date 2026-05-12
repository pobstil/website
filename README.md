# Photo Viewer

A clean, minimal photo viewer for GitHub Pages. Photos rotate randomly on a timer, with manual controls and keyboard navigation.

## Setup

### 1. Add your photos

Drop your image files into the `photos/` folder:

```
photos/
  photos.json
  holiday-1.jpg
  holiday-2.jpg
  portrait.jpg
  ...
```

Supported formats: `.jpg`, `.jpeg`, `.png`, `.webp`, `.gif`

### 2. Update the manifest

Edit `photos/photos.json` to list your photos:

```json
{
  "photos": [
    {
      "src": "holiday-1.jpg",
      "caption": "Somewhere sunny"
    },
    {
      "src": "portrait.jpg",
      "caption": "Golden hour"
    }
  ]
}
```

- **`src`** — filename (inside the `photos/` folder)
- **`caption`** — shown below the image (optional; falls back to filename)

That's it — no code changes needed. Just update the JSON and push.

### 3. Deploy to GitHub Pages

1. Push this folder as a GitHub repository (or add it to an existing one)
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch** → `main` → `/ (root)`
4. Your site will be live at `https://yourusername.github.io/your-repo/`

## Controls

| Action | How |
|--------|-----|
| Next photo | Click **Next →** or press `→` |
| Previous photo | Click **← Prev** or press `←` |
| Pause/resume | Click **Pause** or press `Space` |
| Jump to photo | Click a dot below the image |

## Configuration

Two settings at the top of `index.html` (inside the `<script>` tag):

```js
const INTERVAL_MS = 8000;   // Seconds between auto-advances (8000 = 8s)
const PHOTOS_FILE = 'photos/photos.json';  // Path to manifest
```

## File structure

```
index.html          ← the website (don't need to edit this)
photos/
  photos.json       ← edit this to manage your photos
  photo-1.jpg       ← your images go here
  photo-2.jpg
  ...
README.md
```
