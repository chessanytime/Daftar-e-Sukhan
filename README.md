# Daftar-e-Sukhan — Poetry Archive

A vintage-inspired, responsive poetry website for two collections:

- **Naveen Chourey** — poems by Naveen Chourey.
- **My Favourite Poems** — a personal anthology of poems by other poets and writers.

The site supports Hindi (Devanagari) and English, poem search, language filtering, title sorting, individual poem reading views, and locally saved favourites.

## Add a poem

Open `poems.json` and add an object to either the `naveen` or `favourites` array.

Example:

```json
{
  "naveen": [
    {
      "id": "naveen-poem-001",
      "title": "Poem title",
      "author": "Naveen Chourey",
      "language": "Hindi",
      "category": "Nazm",
      "preview": "A short opening line or two…",
      "text": "Paste the complete poem here.\nKeep the original line breaks.",
      "date": "2026-11-17",
      "note": ""
    }
  ],
  "favourites": [
    {
      "id": "favourite-poem-001",
      "title": "Poem title",
      "author": "Poet's name",
      "language": "English",
      "category": "Poem",
      "preview": "A short opening line or two…",
      "text": "Paste the complete poem here.\nKeep the original line breaks.",
      "date": "2026-11-17",
      "note": ""
    }
  ]
}
```

### Field guide

- `id`: unique ID for every poem; do not reuse IDs.
- `title`: poem title.
- `author`: poet's name.
- `language`: exactly `Hindi` or `English`.
- `category`: optional label, for example Ghazal, Nazm, Geet, or Poem.
- `preview`: short excerpt shown on the collection card.
- `text`: full poem. Use `\n` for line breaks in JSON strings.
- `date`: date in YYYY-MM-DD format; used for recently-added sorting.
- `note`: optional note shown below the poem.

Keep valid JSON syntax: use double quotes around keys and text, and separate objects with commas. Do not put a comma after the final object in an array.

## Publish with GitHub Pages

1. Open this repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch **main** and folder **/(root)**, then save.
5. GitHub will provide the published website address in the Pages section once deployment finishes.

The site is a static website and does not need a server or database. Each update to `index.html` or `poems.json` is committed to GitHub and then published by Pages.

## Notes

- Saved-heart selections are stored in the visitor's own browser using local storage; they are not synced between devices.
- Poems are intentionally not prefilled. Add only the texts you want to publish, and ensure you have permission to share poems that are not your own.
- The Google Fonts connection is used for the literary typography. The site remains readable with fallback fonts if the fonts cannot load.
