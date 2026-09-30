# IMD film delivery notes

- Film: `imd-film.mp4` — 15.000 seconds, 1920 × 1080, 16:9, 30 fps.
- Video: H.264, `yuv420p`, in MP4 with the `moov` atom before `mdat` for browser playback.
- Audio: AAC, 48 kHz stereo. A quiet synthesized electronic pulse builds to a harmonic lift at the IMD reveal. There is no voiceover.
- End card: `imd-end-card.png`, 1920 × 1080, extracted from the 450th encoded frame (index 449, the last frame).
- Footage tool and model: original procedural 2D motion graphics drawn with Python/Pillow 10.2.0 and encoded with FFmpeg 7.0.2 (`libx264` and AAC). No generative footage model, outside image, outside footage, or real person was used.
- Limitations: DejaVu Sans Mono Bold substitutes for IBM Plex Mono; camera moves are 2D glides and zooms. The circuit and quorum beats, exact captions, 0.3-second scene crossfades, and last-two-second URL are included.

Checked locally with `ffprobe`: video codec `h264`, pixel format `yuv420p`, 1920 × 1080 at 30 fps; audio codec `aac`, 48 kHz stereo; total duration `15.000000` seconds. The film is 6,549,691 bytes. The MP4 atom order begins `ftyp`, `moov`, `mdat`. The decoded last frame was visually inspected and saved as the PNG.
