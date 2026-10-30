# Changelog

Entries below describe changes that were actually run, not planned work.
Earlier history was not recorded; this file starts at the first verified
baseline.

## 0.3.0 — 2026-10-30 — first public beta

The 0.3.0 build is the first APK published outside the private beta group.
No feature code changed for this release; it packages the verified 0.3.0
build for public download.

- Public beta APK published for Android 9.0+.
- SHA-256 is listed on the release page and in the asset notes.
- `sh gradlew :app:testDebugUnitTest`: BUILD SUCCESSFUL.
- 11 suites, 128 tests, 0 failures, 0 errors (read from the JUnit XML).
- Covered: DSP, pattern and edit snapshots, undo, recording, levels, pad
  performance, `.ncbeat` fixtures and format, WAV export and project
  serialization.

Known gap recorded, not fixed: `app/src/main/cpp/oboe_stream.cpp` still has a
`TODO(step 2 audit)` for reopening the audio stream on device routing changes.
That path cannot be verified off-device. Use wired output for now.

## 0.2.0 — 2026-10-24 — sampling and patterns

- 16-pad banks with per-step ratchet, probability and swing.
- Four onboard synths and the shared FX chain.
- Sample import and kit mapping.

## 0.1.0 — 2026-10-18 — first internal build

- Native C++17 playback engine and Kotlin pattern model.
- Basic step grid and pad performance.
