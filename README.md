# Lingua Shelf

A small, community-friendly guide for language learners: **books** about a language's history by authors rooted in it, and **movies/series** that show the language at its best, with the **platform** each is available on (no links).

Languages so far: Spanish, French, German, Japanese, Hindi, Korean.

## Run it

It's a static site. Fetching JSON needs a server:

```bash
python -m http.server   # then open http://localhost:8000
```

To host it free, enable **GitHub Pages** on the `main` branch (Settings → Pages).

## Add a language or title

All content lives in `data/languages.json`. Copy an existing language block:

```json
"Italian": {
  "native": "Italiano", "accent": "#15803d",
  "books":  [{"title": "", "author": "", "type": "history|literature", "why": ""}],
  "movies": [{"title": "", "year": 0, "platforms": ["Netflix"], "why": ""}]
}
```

Guidelines:
- Books: mix language-history titles with works by native/rooted authors.
- Movies: pick films where the language is a central part of the beauty.
- Platforms: name the service, never a link. Availability varies by country, so write "Rent/buy" or "Check JustWatch" when unsure.
- Keep `why` to one sentence.

## Ideas for later
Filter by level, add a country selector for platforms, add podcasts and music, validate the JSON in CI.

## License
MIT
