# Skills used

This repository holds no code: each song ships as a GitHub Release. The list below is read from the
releases' `meta.json` and notes.

## Tools
- **MiniMax Music 2.0** (via fal) for the song audio, best of several takes
- **FLUX1.1 pro ultra** (via fal) for the cover image, upscaled to 3000×3000 with the title typeset afterwards
- EBU R128 loudness measurement (integrated loudness, loudness range, true peak)
- **faster-whisper** (`small.en`, int8) speech recognition for the lyric check
- **GitHub Releases** for publishing

## Techniques
- Prompted generation with original lyrics and no artist or song references
- Take selection (best of N)
- Loudness mastering to -14 LUFS with linear gain only, true-peak ceiling at -1 dBTP
- Silence-hole detection inside the track
- Lyric word-recall scoring from an ASR transcript
- Per-release machine-readable metadata (`meta.json`) with cost and QC numbers
