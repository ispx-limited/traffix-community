# Dataset

`events.json` is written by traffix after every decision and holds every
published event. It is not edited here.

```json
{
  "traffix_version": "0.3.0",
  "site": "https://traffix.ispx.co",
  "events": [
    {
      "id": 123,
      "title": {
        "id": 45,
        "name": "Harbour Quest",
        "slug": "harbour-quest",
        "steam_app_id": 123456,
        "image_url": null
      },
      "kind": "game_release",
      "name": "Harbour Quest",
      "version": null,
      "platforms": ["pc", "playstation"],
      "starts_at": "2026-12-01T00:00:00+00:00",
      "date_precision": "day",
      "size_gb": 85.5,
      "popularity_tier": "high",
      "impact_score": 56,
      "summary": "A big release.",
      "published_at": "2026-11-20T18:04:11+00:00",
      "updated_at": "2026-11-20T18:04:11+00:00"
    }
  ]
}
```

| Field | Meaning |
|---|---|
| `kind` | `game_release`, `game_update`, `preload` or `platform_update` |
| `name` | the event's own name: the game for a release, the patch or season for an update |
| `platforms` | from `pc`, `playstation`, `xbox`, `switch`, `windows`, `macos`, `ios`, `android`, `linux` |
| `starts_at` | when the download becomes available, UTC |
| `date_precision` | how exact `starts_at` is: `day`, `hour` or `exact` |
| `size_gb` | gigabytes, `null` when unknown |
| `popularity_tier` | `low`, `medium`, `high`, `massive`, or `null` |
| `impact_score` | 0 to 100, from size and popularity |
| `published_at` | when the event was approved |
| `updated_at` | the last correction |

Events are ordered by `starts_at`. Retired events are not included.
