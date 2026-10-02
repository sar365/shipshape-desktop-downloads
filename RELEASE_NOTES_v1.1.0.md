# DJ Companion 1.1.0 — Windows x64

DJ Companion 1.1.0 adds an offline music library, editable crates, and a native Windows WAV set recorder. Your music files remain in their existing locations; DJ Companion stores its library index and organization data locally.

## What's new

### Local music library

- Add one or more music folders and scan them recursively for AAC, AIFF/AIF, ALAC, FLAC, M4A, MP3, OGG, Opus, WAV, and WMA audio files.
- Read available tags and duration, then browse and search tracks with sorting, pagination, folder filters, and file-availability status.
- Save personal title, artist, album, BPM, key, and notes overrides without rewriting embedded file tags.
- Rescan folders, cancel scans, identify missing files, and reveal available tracks in File Explorer.
- Forget a track from the index or stop tracking a folder without deleting audio files.

### Crates

- Create, rename, color, describe, and delete local crates.
- Search the library while adding tracks, remove crate membership, and reorder tracks.
- Removing tracks from crates or deleting a crate does not delete the library track or its audio file.

### Native Windows set recorder

- Record the default Windows playback endpoint with WASAPI loopback, or select an installed ASIO driver and its input channel or pair.
- Capture directly to uncompressed WAV. WASAPI preserves the endpoint mix format; ASIO uses a driver-supported standard rate and floating-point input audio.
- Monitor stereo peak levels in dBFS, clipping indication, elapsed time, active device and format, and bytes written.
- Write audio through a bounded background buffer and finalize the WAV on normal stop.
- Save timestamped recordings in the Windows Music folder under `DJ Companion Sets`; completed recordings are automatically added to the local library.
- If the app is closed during recording, choose whether to keep recording or stop, finalize, and quit.

## Offline and local data

- Library indexes, metadata overrides, crates, and crate membership are stored in a local SQLite database.
- Folder scanning and crate organization work without an account or internet connection. Music files stay in place and are not uploaded.
- Completed recordings remain on the device and are indexed locally.

## Windows and audio notes

- The native recorder is available in the Windows x64 desktop app. WASAPI requires a default Windows playback endpoint; ASIO requires a compatible installed driver with available input channels.
- ASIO captures the selected interface input; it does not capture audio another application is playing. Some ASIO drivers may be held exclusively by another application.
- WASAPI loopback records the playback mix delivered by the selected default endpoint. Uncompressed WAV does not guarantee bit-perfect capture, and the recorder cannot repair clipping already present in the captured signal.
- This installer is unsigned. Windows may show an Unknown Publisher or SmartScreen warning.

## Release scope

This release includes the local library, crates, and native Windows recorder. A setlist editor and live set-session/timer interface are not included in version 1.1.0.

## Source and distribution

This downloads repository distributes compiled installer binaries and release documentation only. The application source code remains in the private source repository. Binary-only distribution does not prevent Electron application code from being extracted or modified in a local copy.
