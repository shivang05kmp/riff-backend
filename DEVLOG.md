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

## 2026-11-23: Setup (restart)

**Did:** installed Homebrew and Homebrew's bash 5.3. Installed SDKMAN and Temurin JDK 25.0.5.1 (checked with `java -version` and `sdk current java`).
**Learned:**
- JDK: Its a toolbar which u need to run/build java or kotlin code. Compiler (javac) - converts source code to byte code. JVM - the runtime that executes the source code. Has standard libaries like java.util, java.time etc. SpringBoot runs on it the same way Android App runs on ART
- SDKMAN: a version manager for JDKs (also Gradle, Kotlin, Maven). It installs versions side by side and points `java` on my PATH at the current one, so each project can use the Java it needs without uninstalling anything (`sdk use` = this terminal, `sdk default` = every terminal). Like Android Studio's SDK Manager keeping several API levels.
- Why the installer failed: bash in an old shell still meant macOS's /bin/bash. A new tab, or the full path /opt/homebrew/bin/bash, gets the new one.
- **Stuck on:** the SDKMAN installer failed because `curl … | bash` ran macOS's built-in bash 3.2, and SDKMAN needs bash 4 or newer. Fixed it by piping the installer to Homebrew's bash: `| /opt/homebrew/bin/bash`.
**Next:** Setup step 3: check Docker Desktop has 8 GB, Bruno and k6 run. Then step 5 (Ollama: `/api/embed` prints 768) and step 6 (Docker hands-on).

## 2026-11-05: Setup

**Did:** installed JDK 25 (Temurin via SDKMAN), IntelliJ IDEA, Docker Desktop (8 GB memory), Bruno, k6 and Ollama with `qwen2.5:3b` and `nomic-embed-text`. Split Riff into two repos, `riff-backend` and `riff-android`.
**Next:** Prep 1.
