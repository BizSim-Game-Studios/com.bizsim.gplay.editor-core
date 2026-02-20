# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.3] - 2026-02-18

### Changed
- Removed 4 `#if UNITY_2023_1_OR_NEWER` dead code blocks from `BizSimDefineManager.cs` — min Unity is 6000.3, so `#else` branches (deprecated `GetScriptingDefineSymbolsForGroup`) were unreachable
- Replaced `Enum.GetValues(typeof(BuildTargetGroup))` with explicit platform array (`Android, iOS, Standalone, WebGL`) — avoids iterating obsolete/internal enum values

## [0.1.2] - 2026-02-17

### Fixed
- Handle null Firebase version in Package Dashboard (displays "Installed" instead of "Installed (v)")

## [0.1.1] - 2026-02-09

### Added
- `.gitattributes` for consistent line endings across platforms

---

## [0.1.0] - 2026-02-07

### Added

- `PackageDetector` — Instant assembly detection via `AppDomain.GetAssemblies()` scanning
- `BizSimDefineManager` — `BIZSIM_FIREBASE` scripting define management across all platforms
- `BizSimPackageDashboard` — Unified Editor window for BizSim and Google Play package status
- Firebase Analytics detection with version reporting
- Support for Android, iOS, and Standalone build targets
