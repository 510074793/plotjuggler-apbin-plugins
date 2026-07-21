# PlotJuggler 3.16.0 DataAPBin macOS ARM64 build

This repository uses GitHub Actions on an Apple Silicon macOS runner to build:

- the standalone ArduPilot DataAPBin plugin for PlotJuggler 3.16.0;
- a self-contained PlotJuggler 3.16.0 app bundle with the plugin installed.

Build outputs are unsigned community artifacts. See the workflow artifact README for installation details.

CI target: PlotJuggler tag `3.16.0` on GitHub's `macos-15` M1 runner.

Build retry: use an isolated Python environment for Conan.

Build retry: force the Qt 5 keg CMake package to avoid a stale system symlink.

Build retry: pass the exact PlotJuggler CMake package directory to the plugin build.
