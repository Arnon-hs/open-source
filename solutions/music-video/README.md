# Music Video Generator

[![Repository](https://img.shields.io/badge/repository-Arnon--hs%2Fmusic--video-181717?logo=github)](https://github.com/Arnon-hs/music-video) [![Videos](https://img.shields.io/badge/videos-AtlasRepo-FF0000?logo=youtube)](https://www.youtube.com/@ATLASREPO) [![License](https://img.shields.io/badge/code-PolyForm%20Noncommercial%201.0.0-3155ff)](https://github.com/Arnon-hs/music-video/blob/main/LICENSE)

> A local-first CLI and read-only web dashboard for generating instrumental music, assembling one-hour same-genre playlist videos, reviewing media, and preparing private Postiz/YouTube drafts.

## The problem

AI music demos often stop at a single prompt or model-specific script. A practical creator workflow also needs repeatable genre presets, predictable output paths, resumable long jobs, exact video duration, visible progress, media preview, remote GPU guidance, and a guarded handoff to publishing.

## The solution

`Arnon-hs/music-video` provides one entry point for the complete workflow:

```bash
./music-video doctor
./music-video genres
./music-video generate --backend ace-step --genre electronic --duration 60 --dry-run
./music-video playlist --backend ace-step --genre lofi --image assets/images/cover.jpg --dry-run
./music-video web
```

The project supports MusicGen, ACE-Step, DiffRhythm 2, and Stable Audio 3 adapters; 12 instrumental genre presets; single-track audio/video generation; varied one-hour playlists with crossfades; FFprobe validation; a browser dashboard; and private-draft Postiz integration.

## Why it is useful

- one CLI instead of separate commands for every model and media stage;
- safe `--dry-run` before model time, downloads, or GPU cost;
- resumable playlist generation that reuses duration-validated tracks;
- one fitted image without crop or stretching in the final 1280×720 video;
- live progress, logs, validated audio/video previews, and publication state;
- local Apple Silicon instructions plus RunPod, Vast.ai, and GPU VPS guidance;
- English, Russian, and Simplified Chinese documentation and dashboard UI.

## Boundaries and adoption checks

- The repository is code-only: model weights, generated media, credentials, and third-party checkouts are not bundled.
- The code license is PolyForm Noncommercial 1.0.0. Each model, checkpoint, image, audio result, and API keeps its own terms.
- MusicGen is explicitly treated as a non-commercial demo backend. Other models still require checkpoint, training-data, output-rights, and Content ID review.
- The web dashboard is read-only and has no application login. Keep it on loopback, behind an SSH tunnel, or inside a restricted Tailscale tailnet; do not expose it directly to the public internet.
- Postiz creates a private draft only. A successful publication state requires a returned post ID and manual review before publishing.
- One-hour generation is resource-heavy. Run `./music-video doctor`, inspect the hardware guide, and start with a short dry-run.

## Documentation and community

- [English guide](https://github.com/Arnon-hs/music-video#readme)
- [Русская инструкция](https://github.com/Arnon-hs/music-video/blob/main/README.ru.md)
- [简体中文说明](https://github.com/Arnon-hs/music-video/blob/main/README.zh-CN.md)
- [AtlasRepo website](https://atlasrepo.com/)
- [AtlasRepo forum](https://forum.atlasrepo.com/)
- [AtlasRepo videos and demos](https://www.youtube.com/@ATLASREPO)

## Русский

Music Video Generator объединяет генерацию инструментальной музыки, часовую подборку из разных треков одного жанра, монтаж с одной картинкой, проверку результата, web-dashboard и приватный черновик Postiz. Начинайте с `doctor` и `--dry-run`; не публикуйте результат до проверки лицензий моделей, прав на изображения и ручного просмотра готового видео.

## 简体中文

Music Video Generator 将纯器乐生成、同流派的一小时多曲目播放列表、单图视频合成、结果验证、Web dashboard 和 Postiz 私密草稿整合到一个 CLI 中。请先运行 `doctor` 和 `--dry-run`，并在发布前检查模型许可证、图片权利和完整成品。

---

[← All AtlasRepo community solutions](../) · [Open the repository →](https://github.com/Arnon-hs/music-video)
