# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static landing site for **MICI Suivi**, an Android app for tracking Crohn's disease / ulcerative colitis. The site is hosted as-is (no build step) and consists of two French-language HTML files.

## Structure

- `index.html` — Landing page (centered card, app description, feature badges)
- `privacy-policy.html` — Full privacy policy (French, dated, links back from index)

## Development

No build system, no dependencies. Open files directly in a browser or serve locally:

```bash
python3 -m http.server 8080
```

## Design system

Both pages share the same inline CSS conventions:

- **Brand color:** `#5B8A78` (green)
- **Background:** `#F7F7F2`
- **Text:** `#2D3748` (headings), `#718096` / `#4A5568` (body)
- **Accent block:** `.highlight` — left-bordered `#5B8A78`, background `#E8F4F0`
- System font stack: `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`

Styles are kept inline per page; there is no shared stylesheet.

## Key content facts

- Contact email: `micisuivi.app@gmail.com`
- AI analysis uses a proxy server on Railway (Europe), which calls the Anthropic Claude API — no raw user entries leave the device, only aggregated stats or meal text/photo.
- No user accounts, no tracking SDKs, no ads.
- Android permissions used: Camera, Storage/media.
- App not intended for users under 16.
