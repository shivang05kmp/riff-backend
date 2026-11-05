# Riff backend

Riff is a Spotify-like music streaming system, built from scratch as a backend learning project.
Users can upload tracks, stream them, build playlists, search, get recommendations and listen together in real time.
This repo is the server side. The Android client lives in [riff-android](https://github.com/shivang05kmp/riff-android).

**Status:** setup. Nothing is built yet; see [DEVLOG.md](DEVLOG.md) for day-by-day progress.

## Tech stack

- **Language and framework:** Kotlin 2.x on Java 25, Spring Boot, Gradle (Kotlin DSL)
- **Data:** PostgreSQL (+ pgvector), Redis, Kafka (KRaft mode), MinIO (S3-compatible file storage)
- **Media:** FFmpeg to transcode audio into HLS, nginx to serve it like a CDN
- **AI:** Ollama running local models, Spring AI
- **Operations:** OpenTelemetry, Prometheus, Grafana, Tempo, Docker Compose, kind (local Kubernetes), GitHub Actions

Everything runs on this laptop. There is no paid cloud.

## Run it locally

Prerequisites (installed during Setup):

| Tool | Check it works |
| --- | --- |
| JDK 25 via SDKMAN | `java -version` |
| Docker Desktop, 8 GB memory | `docker run --rm hello-world` |
| Ollama with `qwen2.5:3b` and `nomic-embed-text` | `ollama list` |
| k6 | `k6 version` |
| Bruno (API client) | open the app |

How to start the backend will be added on Day 2.

## Repository guide

- [DEVLOG.md](DEVLOG.md): one entry per study day
- [CONTRIBUTING.md](CONTRIBUTING.md): branches, commits and pull requests
- [docs/](docs/README.md): requirements, design decisions and runbooks
