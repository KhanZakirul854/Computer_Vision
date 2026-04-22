# Property Image Tagger Demo

This repository contains a frontend prototype for tagging exterior property violations on images. The demo was prepared to support an academic audit/final presentation around a broader property-violation workflow involving image capture, tagging, and later system integration.

## What This Repo Contains

- `tagging-ui/`
  - standalone frontend prototype
  - image upload
  - zoom and pan
  - multi-violation tagging per image
  - bounding-box editing
  - JSON export
- `docs/`
  - setup and run instructions
  - project summary
  - contribution notes
- audit/project handoff drafts

## Current Scope

This repo currently includes the standalone UI layer only. It does **not** yet include:

- Salesforce integration
- authentication/login
- database storage
- case creation
- GoPro video ingestion pipeline

## Quick Start

1. Clone the repo from GitHub.
2. Open the folder in VS Code.
3. Open `tagging-ui/index.html` in a browser, or use the VS Code `Live Server` extension.

Full instructions are in [docs/SETUP.md](/Users/khanzakirul/Documents/Codex/2026-04-22-hey-ai-so-i-will-give/docs/SETUP.md).

## Dependencies

There are no required package dependencies for this prototype.

You only need:

- Git
- VS Code or another editor
- a modern browser

Optional:

- VS Code `Live Server` extension for easier local preview

## Key Features

- upload real JPG/PNG images
- use a demo image for presentation
- draw multiple violation regions on a single image
- assign a violation after drawing each region
- edit existing saved tags
- pan and zoom while reviewing the image
- export structured JSON annotations

## Demo Notes

This project is presentation-ready as a local frontend prototype. For an audit/demo, the recommended flow is:

1. load an image
2. zoom/pan to the relevant area
3. draw one or more regions
4. assign violations to each region
5. edit one saved violation to show correction support
6. export JSON

## Additional Documents

- [docs/PROJECT_SUMMARY.md](/Users/khanzakirul/Documents/Codex/2026-04-22-hey-ai-so-i-will-give/docs/PROJECT_SUMMARY.md)
- [docs/CONTRIBUTIONS.md](/Users/khanzakirul/Documents/Codex/2026-04-22-hey-ai-so-i-will-give/docs/CONTRIBUTIONS.md)
- [AUDIT_PACKET.md](/Users/khanzakirul/Documents/Codex/2026-04-22-hey-ai-so-i-will-give/AUDIT_PACKET.md)
- [PROJECT_BOOK_DRAFT.md](/Users/khanzakirul/Documents/Codex/2026-04-22-hey-ai-so-i-will-give/PROJECT_BOOK_DRAFT.md)
