# Media for Instagram

Public GitHub Pages repo. Instagram fetches the Reel videos from `https://<user>.github.io/<repo>/reels/<file>.mp4`.

- Put each video into `reels/` and add its post time (UTC) to `reels/schedule.json`, e.g. `{"ig_clip_001.mp4": "2026-11-20T23:00:00Z"}`.
- The workflow `cleanup.yml` runs every 3 hours and deletes every file 3 hours after its post time, so the repo stays small. Files without an entry are never touched.
- Thumbnails/covers can live in `thumbs/` (not cleaned up).
