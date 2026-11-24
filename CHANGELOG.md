Nocturne M3U Manager — Changelog

Version 1.6.4

Interface Improvements

- Reorganized library action buttons into a responsive grid.
- Standardized button sizing, height, spacing and alignment.
- Improved mobile layout with two-column button arrangement and wider-screen layout with three columns.
- Improved text wrapping and toolbar organization to prevent uneven button rows.

Preserved Features

- Retained all 1.6.3 functionality, including group-specific bulk selection, metadata editing and library management.

---

Version 1.6.3

Group Selection Improvements

- Added Select all / Deselect all inside individual album, artist and genre views.
- Selection applies only to tracks belonging to the currently opened group.
- Search-aware selection preserves tracks selected outside the current group or search results.
- Improved selection controls across library views.

---

Version 1.6.2

Library Selection

- Added Select all / Deselect all to Songs, Albums, Artists and Genres views.
- Selection respects the active search.
- Deselecting visible results preserves selections outside the current search.
- Selection button labels update automatically based on the current selection state.

---

Version 1.6.1

Metadata Editor Improvements

- Added metadata field suggestions based on values already present in the scanned music library.
- Added a curated list of common genre suggestions.
- Suggestions are optional; custom values can still be entered freely.
- Applied suggestions to both individual and batch metadata editing.

Library Cleanup

- Removed the standalone "Show tracks without genre" filter button.

---

Version 1.6.0

Metadata Editor

- Added individual metadata editing for library tracks.
- Added support for editing title, artist, album, album artist, genre, year, track number, disc number, composer, comment, copyright, publisher/label, BPM and grouping.
- Added metadata change preview and an option to clear empty fields.
- Added embedded album artwork replacement and removal.
- Added the ability to copy metadata and artwork from one track to selected tracks.

Batch Editing

- Added batch metadata editing for manually selected tracks.
- Added ZIP export of edited copies while preserving relative folder structure.
- Added automatic track numbering based on the current library order.

File Safety

- Edited tracks are exported as new copies.
- Original source files are never overwritten.
- Metadata editing does not intentionally re-encode audio.

---

Version 1.5.0

Playlist Organization

- Added advanced playlist sorting by artist, album, title, track number, release date, release year, duration and filename.
- Added combined Artist → Album → Track Number sorting.
- Added ascending and descending sorting, order inversion and restore original order.
- Added drag-and-drop playlist reordering.
- Playlist order is preserved during M3U export.

Metadata and Track Information

- Expanded library information with release date/year, duration, codec, sample rate and bit depth when available.
- Added detailed track information, including metadata tags, embedded artwork, audio properties and file information.
- Added local caching for expanded metadata.

M3U Compatibility

- Expanded playlist compatibility checks for suspicious paths, duplicate entries, whitespace issues and unmatched tracks.
- Added possible filename match suggestions when a music folder is loaded.
- Added actual track duration to #EXTINF export when available.

---

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

- All existing library browsing, search, sorting, playlist management, M3U export, artwork display, diagnostics, persistent metadata caching and theme customization features remain available.

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
