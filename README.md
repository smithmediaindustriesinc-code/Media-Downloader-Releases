# Media Downloader — Releases

Distribution point for **Media Downloader** installers. **No source code lives here** — the
source is in the private `Media-Downloader` repo.

## What's here

- **[Releases](../../releases)** — one per version, each with its `MediaDownloaderSetup<ver>.exe`
  attached. Non-prerelease = stable; prerelease = beta/preview.
- **[`versions.json`](versions.json)** — the manifest the unified installer reads (version,
  channel, date, download URL, notes), newest first.

## Installing

Download **`MediaDownloaderSetup.exe`** (the unified installer) — it lets you pick which version
to install (latest stable by default; tick "Show beta / pre-release builds" for previews) and
fetches it from here. Or grab a specific version's installer straight from its
[Release](../../releases).

## For maintainers

The private repo's version-bump / release step publishes each built installer here as well:

```
gh release create v<ver> "<path to MediaDownloaderSetup<ver>.exe>#MediaDownloaderSetup<ver>.exe" \
  --repo smithmediaindustriesinc-code/Media-Downloader-Releases --title "<ver>" [--prerelease]
```

then prepend the new entry to `versions.json` and push.
