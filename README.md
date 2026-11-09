# File Converter

A free, unlimited file converter that runs entirely in your browser. No uploads, no sign-up, no limits — your files never leave your device.

**Live:** https://ashraf2706.github.io/file-converter/

## Supported conversions

| Input | Output |
|---|---|
| Video (MOV, MP4, WebM, AVI, MKV, 3GP, …) | MP4 (fast remux or full re-encode), MP3 / WAV audio extraction |
| Audio (MP3, WAV, M4A, OGG, FLAC, …) | MP3, WAV, M4A |
| Images (PNG, JPEG, WebP, GIF, BMP, SVG) | PNG, JPEG, WebP (with quality slider) |
| CSV / TSV | JSON, CSV, TSV, TXT |
| JSON | CSV, pretty-printed JSON, minified JSON |
| TXT / MD / HTML | TXT, MD, HTML |

## Features

- Drag & drop or click to pick files
- Batch conversion ("Convert all")
- Quality slider for JPEG/WebP output
- Video/audio powered by a self-hosted [ffmpeg.wasm](https://github.com/ffmpegwasm/ffmpeg.wasm) (~31 MB, loaded only when you convert a video, cached after the first use)
- "MP4" first tries a near-instant stream copy (perfect for iPhone .mov files) and automatically falls back to a full re-encode if the codecs aren't MP4-compatible
- Dark/light mode follows your system setting
- 100% client-side

## Running locally

Serve the folder (e.g. `python3 -m http.server`) and open it in a browser. Image/data conversions also work by just opening `index.html` directly; video conversion needs the page served over http(s) because it uses a web worker.
