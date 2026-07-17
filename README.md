<div align="center">

<!-- Replace the URL below with the GitHub-hosted Ember logo URL. -->

<img src="docs/images/ember-logo.png" alt="Ember Logo" width="180">

# Ember

### A modern asset development SDK for legacy EA Sports titles

**C++20 · Qt 6 · NCAA Football 14 · College Football Revamped**

</div>

---

## Overview

**Ember** is an open-source software development kit and desktop asset workspace for researching, inspecting, editing, and rebuilding resources from legacy EA Sports titles.

Development currently centers on **NCAA Football 14** and the **College Football Revamped** ecosystem. Ember provides the technical foundation for archive tooling, asset editors, game-specific workflows, project management, and future community modding infrastructure.

The project was previously developed under the names **ASTra-Core** and **CFBRevamped SDK**.

> **Development Status:** Active development
> **Current Focus:** Stabilization, architectural migration, and the Ember 1.4 Asset Workspace
> **Production Readiness:** Experimental; APIs and project structure may change

---

## Naming and Migration Status

The project is currently transitioning from **ASTra-Core** and **CFBRevamped SDK** to **Ember**.

The public source tree may still contain legacy identifiers, including:

* `ASTra`
* `astra.exe`
* `CFBRevamped SDK`
* `gf_*` libraries and executables
* Historical directory and namespace names

These identifiers will be migrated incrementally as the architecture is stabilized. Their presence does not indicate that the Ember rebrand has been abandoned.

This staged approach avoids unnecessary code churn while active editor, archive, workspace, and rendering systems are being completed.

---

## Project Vision

Ember is being designed as an asset-first development environment for legacy game modding.

Rather than functioning only as an archive browser, Ember aims to provide a unified workspace where developers and creators can:

* Organize game installations and modding projects
* Browse archives and game resources
* Search for assets across multiple files
* Preview supported asset types
* Inspect metadata and dependencies
* Extract, replace, and rebuild resources
* Open assets in specialized editors
* Package and distribute complete modifications
* Extend the application through modular tooling

NCAA Football 14 is the initial platform, but the underlying architecture is intended to support additional legacy EA titles where technically practical.

---

## Current Capabilities

### Workspace and Project Management

* Game library management
* Workspace creation and loading
* Recent project tracking
* Project notes
* Favorites and asset history
* Workspace validation
* RPCS3 game discovery and onboarding
* Region-aware game configuration
* Background task infrastructure

### Archive Tooling

* AST archive inspection
* BGFA archive support
* Recursive archive discovery
* Asset extraction
* Archive indexing
* Safe archive rebuilding infrastructure
* Asset naming and lookup systems
* Hash and metadata inspection

### Asset Discovery

* Archive and asset browsing
* Cross-archive search
* File type detection
* Asset metadata inspection
* Editor routing
* Extension-based editor registration
* Command-line research utilities

### Texture Tooling

* Texture extraction
* Texture conversion
* Texture replacement workflows
* XPR2 research and support
* Texture metadata inspection
* Preview infrastructure

### APT and Interface Research

* APT parsing
* Timeline and display-list reconstruction
* Sprite inspection
* Shape and image binding research
* Text and label inspection
* Mask and depth visualization
* Render auditing
* Screenshot export
* UI asset classification

### Model Research

* RSF parsing
* Geometry inspection
* Model export research
* OBJ and glTF export workflows
* Skeleton and mesh analysis
* NCAA Football 14 player asset research

### Application Infrastructure

* C++20 codebase
* Qt 6 desktop interface
* Modular controller architecture
* Reusable editor framework
* Background task management
* Structured logging and diagnostics
* Unit and integration testing
* CMake-based builds

---

## Roadmap

### Ember 1.3.x — UI Renaissance and Stabilization

The 1.3 series established the modern Ember desktop experience and separated application behavior into reusable controllers and services.

Major areas include:

* Redesigned SDK Hub
* Modern game library
* Workspace dashboard
* Native dark interface
* Sidebar navigation
* Local game artwork
* Reusable UI components
* Asset browser improvements
* Editor registration infrastructure
* Search and workspace controller stabilization
* Runtime wiring and regression testing

Some internal identifiers remain under their historical names while the migration continues.

---

### Ember 1.4.0 — Asset Workspace

The 1.4 release will transform Ember into a more complete asset development environment.

Planned areas include:

#### Asset Preview Framework

* Universal preview host
* Preview routing
* Loading and error states
* Unsupported-format handling
* Specialized previews for supported resources

#### Metadata Inspector

* Asset properties
* Archive source information
* File hashes
* Format metadata
* Dependency placeholders
* Contextual actions

#### Asset-Centric Navigation

* Improved asset discovery
* Search result navigation
* Asset history
* Favorites
* Related-resource navigation
* Context-sensitive editor launching

#### Workspace Integration

* Project-aware asset operations
* Source and modified asset separation
* Safer replacement workflows
* Change tracking foundations
* Export and packaging preparation

---

### Future Development

Long-term development may include:

* Rich texture editing workflows
* APT visual editing
* RSF model inspection and editing
* Uniform asset workflows
* Team and league editing
* Dynasty database tooling
* Stadium research and editing
* TeamBuilder-style creation tools
* Mod packaging and installation
* Project dependency tracking
* Plugin and extension support
* Additional legacy EA Sports titles

Future features are research-dependent and are not guaranteed until the necessary game formats and runtime behavior are understood.

---

## Repository Layout

The current repository retains its historical internal naming while the Ember migration is underway.

```text
ASTra-Core/
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

Directory, executable, target, and namespace names may change in future releases as the Ember migration progresses.

---

## Build Requirements

Minimum requirements:

* CMake 3.24 or newer
* A C++20-compatible compiler
* Qt 6
* Git
* zlib
* Ninja or MinGW Makefiles on Windows

Dependencies such as `spdlog`, `nlohmann/json`, and `Catch2` are managed through CMake where supported.

---

## Building on Windows

The exact build command depends on the installed compiler and Qt toolchain.

### Ninja

```powershell
cmake -S . -B build -G Ninja
cmake --build build --target gf_toolsuite_gui
```

### MinGW Makefiles

```powershell
cmake -S . -B build -G "MinGW Makefiles"
cmake --build build --target gf_toolsuite_gui -j 8
```

Ensure that CMake, Qt, and the selected compiler are available in the active environment.

---

## Running

Executable names currently retain their legacy identifiers.

### Desktop Application

```powershell
build\apps\gf_toolsuite_gui\gf_toolsuite_gui.exe
```

### Command-Line Tools

```powershell
build\apps\gf_cli\astra.exe --version
```

Executable names and paths may change during the Ember migration.

---

## Documentation

Project documentation is maintained under the `docs` directory.

Important documents may include:

* `docs/architecture/architecture.md`
* `docs/requirements/requirements.md`
* `docs/detection_rules.md`

Some documentation may still reference ASTra-Core or CFBRevamped SDK until the migration is complete.

---

## Compatibility

Ember currently focuses on research and tooling for:

* NCAA Football 14
* College Football Revamped
* PlayStation 3 game resources
* RPCS3 development environments

Support for other platforms, titles, formats, or game versions should not be assumed unless explicitly documented.

Ember is an independent community project and is not affiliated with or endorsed by Electronic Arts, EA Sports, the NCAA, RPCS3, or the College Football Revamped team.

All trademarks and copyrighted materials belong to their respective owners.

---

## Contributing

Ember is still undergoing significant architectural development. Contribution guidelines, coding standards, and format documentation will be expanded as the project stabilizes.

Before submitting major changes:

1. Review the existing architecture documentation.
2. Keep format parsing separate from interface code.
3. Preserve source assets during write operations.
4. Add tests for parsing, rebuilding, and editor behavior.
5. Clearly document assumptions about undocumented game formats.

Research findings, reproducible test files, format documentation, and targeted bug reports are especially valuable.

---

## License

See [`LICENSE`](LICENSE) for licensing information.
