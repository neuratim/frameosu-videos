# NeuraTiM FrameOSU videos

Public campaign, advertisement and guide videos for NeuraTiM FrameOSU.
This is the independent `neuratim/frameosu-videos` repository, checked out at
`packages/frameosu/videos/`, beside the application's `app/` and presentation `web/`.

Organize media by language code first: `en/`, `cs/`, and other languages as
recordings become available. Within a language use purpose folders such as
`guides/`, `campaigns/` or `advertisements/`, followed by a platform where useful.
Only English Windows guides currently exist; no translations are implied.

`en/guides/windows/` contains twelve native MP4 recordings, WebVTT captions
and the original capture provenance, migrated byte-for-byte from frameosu-web.
The clips include quiet supplied instrumental music and no narration.

After preparing and checking an asset change, commit it locally on main. From
the sibling website run `node scripts/sync-video-reference.mjs ../videos` and
`node scripts/verify-guide-videos.mjs --videos ../videos` after building the site.
The website keeps small caption/provenance snapshots and pins production MP4
URLs to the recorded videos commit. Its dev and preview servers stream this
local checkout with HTTP ranges; deployed pages load the public repository.

Publish the referenced videos commit before publishing a website that uses it.
A local commit alone is unavailable to deployed readers. Pushes and deployment
require explicit authorization. Never include private production inputs here.
