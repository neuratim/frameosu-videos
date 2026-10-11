# FrameOSU videos code map

| Path                                | Responsibility                                                    |
| ----------------------------------- | ----------------------------------------------------------------- |
| `en/guides/windows/*.mp4`           | Twelve English native Windows guide recordings                    |
| `en/guides/windows/*.vtt`           | Matching optional English captions                                |
| `en/guides/windows/provenance.json` | Capture actions, music, motion evidence and video SHA-256 digests |
| `.gitattributes`                    | LF text and binary video handling                                 |

To replace a guide, update its video, captions and provenance together, verify
its size and SHA-256, then refresh the website reference as described in README.
