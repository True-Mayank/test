# LUXE Music

Offline Android music player using a WebView UI and Android Storage Access Framework.

## Features
- Select one local music folder; subfolders are ignored.
- Real embedded MP3 album artwork thumbnails.
- Artwork is extracted natively on Android and sent to the LUXE UI in the background.
- Browser fallback includes a small ID3v2 APIC artwork reader for MP3 files.
- List/grid views.
- Sort menu: title A-Z/Z-A, newest/oldest added, recently played, most played.
- Local favorites, recent songs and playlists.
- Native folder persistence.
- Native foreground playback service foundation.

## GitHub build
Upload this complete project to GitHub and build the `app` module with Android Studio/Gradle.


## UI update
This version uses one Library screen with four category tiles (Tracks, Playlist, Favourite, Recent), a persistent search field, and LUXE Music as the heading. The three-line options menu contains View, Sort Order, and Playing Order. Playlist detail screens have their own search and saved view/sort/playing-order preferences.


## UI and playback fixes in this build
- Browser playback uses the selected local audio files; Android playback sends the queue to the native foreground media service.
- The three-line menu opens the View, Sort Order, and Playing Order options.
- Playlist cards open an individual playlist screen with search, independent view/sort/playing order, add-song selection, play, and remove-from-playlist controls. Removing a song from a playlist does not remove it from the library.
- Customise LUXE opens appearance settings for accent theme, font, preset background, and an image background.
- JavaScript syntax was checked. Please test playback on your device/browser; actual audio format support depends on the platform decoder.


## Added LUXE feature pack
- Rename audio files and delete files from the selected Android folder through the song options menu. These actions require the folder provider to grant write access.
- Per-song Slow Reverb settings with built-in Slow Reverb, Deep Reverb, Dreamy and Ambient presets, plus user-created presets.
- Per-song playback speed from 0.5x to 2.0x.
- Native Android crossfade playback with a 0 to 12 second duration control.
- Potential duplicate finder, grouped by normalized title, artist and file size. It is a review aid, not a guaranteed audio-fingerprint match.
- Dynamic artwork background treatment in the maximized player.
- Full-screen animated visualizer with Bars, Wave, Circle and Particles display modes. The current visualizer is animated artwork and is not a true frequency analyser.
- Maximized-player swipe gestures for next/previous and volume, plus double-tap play/pause on the artwork.
- Music Roulette for all songs or favourites.

The Android APK should be built and tested with the included GitHub Actions workflow. This source archive has been checked for JavaScript syntax, HTML parsing, matching root/asset copies and basic Java source structure, but no Android SDK/Gradle installation was available in this environment, so an APK build or device test has not been claimed.
