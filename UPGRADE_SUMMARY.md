---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.9.4-beta
- **To:** 1.0.0-beta
- **Date:** 2026-03-25
- **Automated changes:** 64
- **Manual steps:** 2

## Automated Changes Applied

### Configuration (2 files)

- [x] Updated _config.yml: max_viewer_cards 10 -> 8
- [x] Updated _config.yml: version 1.0.0-beta (2026-03-25)

### Layouts (6 files)

- [x] Updated _layouts/story.html - Card-stack story layout
- [x] Updated _layouts/default.html - Default layout (CDN links removed)
- [x] Updated _layouts/object.html - Object page with video/audio support
- [x] Updated _layouts/objects-index.html - Gallery with media type thumbnails
- [x] Updated _layouts/index.html - Homepage with media-type-aware thumbnails
- [x] Updated _sass/_layout.scss - Layout styles (gallery thumbnails)

### Includes (4 files)

- [x] Updated _includes/story-step.html - Story step with clip and alt data
- [x] Updated _includes/panels.html - Panels (z-index consolidated)
- [x] Updated _includes/share-button.html - Share button (Lucide SVG)
- [x] Updated _includes/share-panel.html - Share panel (Lucide SVGs)

### Styles (5 files)

- [x] Updated _sass/_story.scss - Card-stack story styles
- [x] Updated _sass/_viewer.scss - Object page viewer styles
- [x] Updated _sass/_panels.scss - Panel styles
- [x] Updated _sass/_share.scss - Share button styles
- [x] Updated _sass/_embed.scss - Embed mode styles

### Scripts (41 files)

- [x] Updated assets/js/telar-icons.js - Lucide SVG icon module
- [x] Updated assets/js/embed.js - Embed mode (Lucide icons)
- [x] Updated assets/js/objects-filter.js - Gallery filter (media_type/medium)
- [x] Updated assets/js/share-panel.js - Share panel (Lucide icons)
- [x] Updated assets/js/story-unlock.js - Password unlock (Lucide icons)
- [x] Updated assets/js/telar-story.js - Bundled story JS
- [x] Updated assets/js/telar-story.js.map - Source map
- [x] Updated assets/js/telar-story/main.js - Story entry point
- [x] Updated assets/js/telar-story/card-pool.js - Card pool manager
- [x] Updated assets/js/telar-story/card-type.js - Card type detection
- [x] Updated assets/js/telar-story/iiif-card.js - IIIF card module
- [x] Updated assets/js/telar-story/text-card.js - Text card module
- [x] Updated assets/js/telar-story/scroll-engine.js - Scroll engine
- [x] Updated assets/js/telar-story/video-card.js - Video card module
- [x] Updated assets/js/telar-story/audio-card.js - Audio card module
- [x] Updated assets/js/telar-story/navigation.js - Navigation module
- [x] Updated assets/js/telar-story/state.js - Shared state
- [x] Updated assets/js/telar-story/viewer.js - Viewer module
- [x] Updated assets/js/telar-story/utils.js - Shared utilities
- [x] Updated assets/js/telar-story/panels.js - Panel module
- [x] Updated scripts/process_audio.py - Audio build pipeline
- [x] Updated scripts/build_local_site.py - Local build script (7-step)
- [x] Updated scripts/generate_collections.py - Collections generator
- [x] Updated scripts/generate_iiif.py - IIIF tile generator
- [x] Updated scripts/telar/core.py - CSV-to-JSON core
- [x] Updated scripts/telar/csv_utils.py - CSV utilities
- [x] Updated scripts/telar/processors/objects.py - Object processor
- [x] Updated scripts/telar/processors/stories.py - Story processor
- [x] Updated scripts/telar/search.py - Search data generator
- [x] Updated package.json - npm dependencies
- [x] Updated tests/js/card-pool.test.js - Card pool tests
- [x] Updated tests/js/card-type.test.js - Card type tests
- [x] Updated tests/js/iiif-card.test.js - IIIF card tests
- [x] Updated tests/js/iiif-lerp.test.js - IIIF lerp tests
- [x] Updated tests/js/text-card.test.js - Text card tests
- [x] Updated tests/js/scroll-engine.test.js - Scroll engine tests
- [x] Updated tests/js/navigation.test.js - Navigation tests
- [x] Updated tests/js/video-card.test.js - Video card tests
- [x] Updated tests/js/audio-card.test.js - Audio card tests
- [x] Updated tests/js/state.test.js - State tests
- [x] Updated tests/js/utils.test.js - Utils tests

### Other (6 files)

- [x] Updated assets/img/background-gris.svg - Weave pattern background
- [x] Updated tests/unit/test_csv_utils.py - CSV utils tests
- [x] Updated tests/unit/test_generate_collections.py - Collections tests
- [x] Updated tests/unit/test_process_audio.py - Audio pipeline tests
- [x] Updated _data/languages/en.yml - English strings (clip_picker keys added)
- [x] Updated _data/languages/es.yml - Spanish strings (clip_picker keys added)

## Manual Steps Required

Please complete these after merging:

1. **If you use GitHub Pages:**

Replace your `.github/workflows/build.yml` with the latest version from the Telar repository. The new workflow adds an audio processing step that runs conditionally when audio files are detected.

Steps:
1. Go to https://github.com/UCSB-AMPLab/telar/blob/main/.github/workflows/build.yml
2. Click the "Raw" button
3. Copy the entire file contents
4. Replace the contents of `.github/workflows/build.yml` in your repository ([guide](https://github.com/UCSB-AMPLab/telar/blob/main/.github/workflows/build.yml))
2. **If you work with your site locally:**

Install JavaScript dependencies:

```
npm install
```

This adds lenis (scroll engine), @vimeo/player (video embeds), esbuild (JS bundler), and vitest (test runner).

**Optional — audio support** (only if your site includes audio objects):

```
brew install ffmpeg audiowaveform      # macOS
sudo apt install ffmpeg audiowaveform  # Ubuntu
```

Sites without audio objects do not need these tools.

## Resources

- [Full Documentation](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
