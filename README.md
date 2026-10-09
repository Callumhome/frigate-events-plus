# Frigate Events Plus

Frigate Events Plus is Callumhome's maintained version of a Home Assistant Lovelace card for browsing Frigate detection events.

It builds on the original MIT-licensed Frigate Events Card project. The original copyright and licence notice are retained in `LICENSE`; inherited code remains subject to that licence.

## Features

- Browse recent Frigate detection events in a responsive gallery.
- Filter events by camera, label and zone.
- View snapshots, bounding boxes and event details.
- Play event clips and use hover previews.
- Optional live camera view using Home Assistant WebRTC or go2rtc.
- Scrollable gallery, grid layouts, daily view reset and modal navigation.
- New Frigate Events Plus features will be developed here.

## Installation

This repository is under active development. Do not treat the current build as a stable release.

After a release, add `frigate-events-plus.js` as a JavaScript module resource in Home Assistant.

## Development

Requirements: Node.js and npm.

```bash
npm install
npm run build
```

The build output is `frigate-events-plus.js`.

## Attribution and licence

This project incorporates code from the original [Frigate Events Card](https://github.com/saihgupr/frigate-events-card), licensed under the MIT License. See `LICENSE` for the required notice and terms.
