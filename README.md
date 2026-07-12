# CFBRevamped SDK

The **CFBRevamped SDK** is a modern C++20 and Qt6 software development kit for EA Sports college football titles, with an initial focus on **NCAA Football 14** and the College Football Revamped project.

The SDK provides reusable libraries, tools, and editors for working with EA Sports archive formats, user interface assets, textures, rosters, and game resources. It serves as the technical foundation for future CFBRevamped tools including archive editors, league editing, TeamBuilder restoration, and other community projects.

> **Project Status:** Released to public, new incremental features  
> APIs, file formats, and project structure are actively evolving.

---

# Goals

The long-term goal of the CFBRevamped SDK is to become the definitive open development platform for EA Sports college football games.

Current development focuses on:

- AST/BGFA archive browsing and editing
- Safe archive rebuilding
- RSF parsing and editing
- Texture extraction, conversion, and replacement
- XPR2 texture workflows
- APT UI parsing and visual inspection
- XML generation and editing
- Command-line tooling for automation
- Qt-based desktop tooling

Future goals include:

- League Editor
- TeamBuilder restoration tools
- Dynasty database editing
- Stadium editing
- Uniform editing
- Mod packaging
- Cross-title SDK support (NCAA, Madden, etc.)

---

# Roadmap

## Phase 1 — SDK Foundation *(Current)*

- Core archive library
- AST/BGFA support
- Safe write pipeline
- RSF support
- Texture library
- APT parser
- XML serialization
- CLI utilities
- Qt desktop application
- Unit testing and validation

---

## Phase 2 — Asset Editing

- Texture replacement
- Archive rebuilding
- APT visual editor
- Preview rendering
- Resource dependency viewer
- Batch processing tools

---

## Phase 3 — League Editor

A complete editor for NCAA Football 14 featuring:

- Teams
- Conferences
- Schedules
- Rosters
- Dynasty databases
- Bowl configuration
- Playoff support
- Season customization

---

## Phase 4 — TeamBuilder

Modern replacement for EA's discontinued TeamBuilder.

Planned capabilities include:

- Uniform editor
- Field editor
- Logo management
- Team branding
- Stadium assignment
- Package import/export

---

## Phase 5 — Expanded SDK

Long-term expansion into additional EA Sports titles, shared SDK libraries, and community modding infrastructure.

Potential support includes:

- Madden
- NCAA Basketball
- Tiger Woods PGA Tour
- Legacy EA Sports archive formats

---

# Project Layout

```text
CFBRevamped-SDK/
├─ apps/
│  ├─ gf_cli/
│  └─ gf_toolsuite_gui/
│
├─ libs/
│  ├─ gf_apt/
│  ├─ gf_core/
│  ├─ gf_models/
│  ├─ gf_platform_ps3/
│  └─ gf_textures/
│
├─ docs/
│  ├─ architecture/
│  └─ requirements/
│
├─ tests/
└─ cmake/
```

---

# Build Requirements

Minimum requirements:

- CMake 3.24+
- C++20 compiler
- Qt 6
- Ninja (recommended)
- Git
- zlib

Dependencies including `spdlog`, `nlohmann/json`, and `Catch2` are automatically downloaded using CMake's `FetchContent`.

---

# Building

## Windows

```powershell
cmake -S . -B out-win
cmake --build out-win --target gf_toolsuite_gui -j 8
```

---

# Running

CLI

```powershell
out-win\apps\gf_cli\astra.exe --version
```

GUI

```powershell
out-win\apps\gf_toolsuite_gui\gf_toolsuite_gui.exe
```

> *(Executable names may change as the project is renamed.)*

---

# Documentation

Additional documentation can be found in:

- `docs/architecture/architecture.md`
- `docs/requirements/requirements.md`
- `docs/detection_rules.md`

---

# Current Status

The CFBRevamped SDK is under active development and is not yet considered production ready.

Current work is focused on strengthening the SDK foundation, improving archive support, modernizing the codebase, and building the infrastructure required for future editing tools.

Development is incremental, with stability and correctness taking priority over rapid feature additions.

---

# License

See `LICENSE`.
