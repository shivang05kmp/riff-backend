# Devlog

One entry per study day, newest first. Keep each entry short; it is a record for future you, not an essay.

Template:

```
## YYYY-MM-DD: <plan item>
**Did:** what you built or set up
**Learned:** 2–3 things that are new to you
**Stuck on:** what went wrong and how you fixed it
**SDE-2 question:** your answer (Day items only)
**Next:** the first thing to do next session
```

---

## 2026-11-05: Setup

**Did:** installed JDK 25 (Temurin via SDKMAN), IntelliJ IDEA, Docker Desktop (8 GB memory), Bruno, k6 and Ollama with `qwen2.5:3b` and `nomic-embed-text`. Split Riff into two repos, `riff-backend` and `riff-android`.
**Learned:** <!-- in your own words: what a JDK, a Docker container and an embedding model are -->
**Stuck on:** the SDKMAN installer failed because `curl … | bash` ran macOS's built-in bash 3.2, and SDKMAN needs bash 4 or newer. Fixed it by piping the installer to Homebrew's bash: `| /opt/homebrew/bin/bash`.
**Next:** Setup step 5 (Docker hands-on), then Prep 1.
