# NeuraTiM FrameOSU videos

Public campaign, advertisement and guide videos for NeuraTiM FrameOSU.
This is the independent `neuratim/frameosu-videos` repository, checked out at
`packages/frameosu/videos/`, beside the application's `app/` and presentation `web/`.

Organize media by language code first: `en/`, `cs/`, and other languages as
recordings become available. Within a language use purpose folders such as
`guides/`, `campaigns/` or `advertisements/`, followed by a platform where useful.
Windows guide recordings are available in all eighteen supported app languages.

Each `<language>/guides/windows/` contains fourteen native MP4 recordings,
translated WebVTT captions and capture provenance. The English folder also
retains its earlier unpublished AI chapter, no longer listed in its provenance.
The October 28–29 sets record app 1.4.1 (the redesigned interface, plus the
Split, Audio and Export a frame chapters) in the optimized Windows app with GPU
capture/encoding at 60 fps, a visible cursor and blue click rings.
Eleven chapters demonstrate playback; picture-only motion checks cover their
moving spans, excluding decoder startup. Original 30 fps
source-frame matching confirms normal playback speed in Parts and Select. Capture
provenance includes every measured span and excludes authored photo holds and
still-image parts. Recording and audit tools live in the sibling app's `tool/`.
The clips include quiet supplied instrumental music. Sixteen languages are
also narrated (October 29): each caption is spoken by the owner's chosen Deepgram
voice (Aura-2 for en, de, es, fr, it and ja; Flux for bn, hi, id, ko, pl, pt, ru,
tr, vi and zh), levelled to about -17 LUFS with the music ducked beneath it.
Where a line needs longer than its moment, the picture holds just before the next
step (never inside a measured playback span), so the narrator always finishes
first; those clips are re-encoded with the original colour tags at about the
original bitrate, and the subtitles follow the voice. Provenance records each
spoken line, its timing and digest, every picture hold and the unnarrated
recording's digest. Arabic and Czech have no voice and keep visible captions.

After preparing and checking an asset change, commit it locally on the requested video branch. From
the sibling website run `node scripts/sync-video-reference.mjs ../videos` and
`node scripts/verify-guide-videos.mjs --videos ../videos` after building the site.
The website keeps small caption/provenance snapshots and pins production MP4
URLs to the recorded videos commit. Its dev and preview servers stream this
local checkout with HTTP ranges; deployed pages load the public repository.

Publish the referenced videos commit before publishing a website that uses it.
A local commit alone is unavailable to deployed readers. Pushes and deployment
require explicit authorization. Never include private production inputs here.
