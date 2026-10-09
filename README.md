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
- Optionally hide events after the full-size modal clip finishes playing (`auto_hide_watched`). Hover previews do not count as watched.
- Optionally hide events covered by Frigate review segments marked as reviewed for the current Frigate user (`auto_hide_reviewed`).
- Watched state is stored locally in the browser. These features only hide cards; they never delete or alter Frigate events, clips, snapshots, or review status.

## Installation

This repository is under active development. Do not treat the current build as a stable release.

For development/testing, add `frigate-events-plus.js` as a JavaScript module resource in Home Assistant (Settings → Dashboards → Resources). Use the raw file URL from this repository, or download the file to `/config/www/` and reference it as `/local/frigate-events-plus.js`. This is still under development, so back up your dashboard before testing.

### Optional YAML options

```yaml
type: custom:frigate-events-plus
frigate_client_id: frigate
auto_hide_watched: true
auto_hide_reviewed: true
```

`auto_hide_watched` and `auto_hide_reviewed` default to `false`. Reviewed-event filtering requires a version of the Frigate Home Assistant integration that supports the `frigate/reviews/get` WebSocket command. If that command is unavailable, the card keeps events visible rather than guessing.

## Development

Requirements: Node.js and npm.

```bash
npm install
npm run build
```

The build output is `frigate-events-plus.js`.

## Attribution and licence

This project incorporates code from the original [Frigate Events Card](https://github.com/saihgupr/frigate-events-card), licensed under the MIT License. See `LICENSE` for the required notice and terms.
