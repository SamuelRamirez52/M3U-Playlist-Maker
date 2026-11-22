Nocturne M3U Manager — Changelog

Version 1.4.4

M3U Playlist Import

- Added support for importing external ".m3u" playlists.
- Added an Import M3U option in the Playlists section.
- Added playlist name recovery from imported files.
- Added support for "#EXTINF" metadata.
- Added support for relative file paths.
- Imported tracks are automatically matched against the loaded music library.
- Unmatched tracks are preserved and marked as not found.
- Added duplicate playlist name protection.
- Existing playlists remain unaffected during import.

Interface Improvements

- Redesigned playlist action buttons for better visibility and accessibility.
- Improved the Sort, Import M3U, New Playlist and Export M3U controls.
- Improved button spacing and layout responsiveness.
- Replaced the original EM header logo with a minimalist moon symbol.
- The moon logo uses adaptive coloring to remain visible across different themes.

Compatibility

- Maintained TagLib-Wasm 2.5.0.
- Preserved existing audio format compatibility, metadata reading and embedded artwork support.

Preserved Features

All existing library browsing, search, sorting, playlist management, M3U export, artwork display, diagnostics, persistent metadata caching and theme customization features remain available.

---

Version 1.4.3

Performance Improvements

- Added parallel audio processing with 3 concurrent workers.
- Significantly reduced library scanning time.
- Improved handling of large music libraries.
- Added progressive library updates during scanning.

Persistent Metadata Cache

- Added IndexedDB-based metadata and artwork caching.
- Library data is restored after page reloads.
- Previously scanned metadata is reused to avoid unnecessary processing.
- Added cache hit and write error tracking.

Library Management

- Added individual track removal.
- Added bulk track removal.
- Tracks can be removed from the library without deleting original audio files.
- Existing playlists remain unaffected when tracks are removed from the library.

Diagnostics

- Added an integrated diagnostics system.
- Added error and warning tracking.
- Added scan duration, metadata read and cache statistics.
- Added diagnostic report export in TXT format.
- Added copy and clear log options.
- Added automatic JavaScript error and unhandled promise rejection logging.
- Diagnostic history is stored locally.

Compatibility

- Maintained TagLib-Wasm 2.5.0.
- Preserved support for compatible audio formats, including FLAC, WAV, MP3, M4A, OGG, APE and DSD.
- Maintained metadata and embedded artwork reading.

Testing Results

Tested with a library containing 506 audio files.

- Initial scan reduced from 5 minutes 48 seconds to approximately 1 minute 2 seconds.
- Approximately 82% reduction in initial scanning time.
- Second scan completed in approximately 30 seconds.
- 506 cache hits and 0 metadata reads on the second scan.
- 505 embedded artworks detected.
- 0 errors and 0 warnings.
- Library restoration, individual removal, bulk removal and playlist preservation successfully tested.

---

Version 1.4.4 introduces M3U playlist importing and interface refinements, building on the performance, caching and library management improvements introduced in version 1.4.3.
