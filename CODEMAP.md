# FrameOSU videos code map

| Path                                        | Responsibility                                                                 |
| ------------------------------------------- | ------------------------------------------------------------------------------ |
| `<language>/guides/windows/*.mp4`           | Fifteen native Windows guide recordings per language, in all eighteen          |
| `<language>/guides/windows/*.vtt`           | Matching translated captions                                                   |
| `<language>/guides/windows/provenance.json` | Capture actions, music, narration, motion evidence and video SHA-256 digests   |
| `en/guides/windows/ai.*`                    | The earlier unpublished English AI chapter, not listed in its provenance       |
| `.gitattributes`                            | LF text and binary video handling                                              |

To replace a guide, update its video, captions and provenance together, verify
its size and SHA-256, then refresh the website reference as described in README.
The provenance records optimized app/GPU recording settings, actual click times,
noise-resistant motion spans and source-frame speed checks. Its motion aggregate
retains the worst measured span. Music metadata records the original track hash,
bounded randomized excerpt, gentle gain and audio fades.
