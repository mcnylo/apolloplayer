![apollo_player](https://github.com/michaelmcniel65/apolloplayer/assets/100385832/af85e666-cd56-4846-a1bb-0dc8b46e57bc)

# Apollo Player

Apollo Player is a desktop music player for Windows. It is written in C# with WPF and uses NAudio for audio playback. The application provides local music-library management, standard playback controls, shuffle, track repeat, seeking, and a custom interface.

**Current version:** 1.1.07

## Features

- Play MP3 and WAV files.
- Play, pause, stop, skip, and restart tracks.
- Move through the library with previous and next controls.
- Continue automatically when a track ends.
- Shuffle tracks without immediately repeating a used track.
- Return to earlier tracks during shuffle playback.
- Repeat the selected track.
- Seek to a different position in a track.
- View the current time and total track time.
- Adjust the volume or mute the audio.
- Import multiple audio files at one time.
- Remove tracks from the local music library.
- Scroll long track names across the current-track display.
- Use a custom borderless WPF interface with embedded images, animation, and fonts.

## Supported Audio Formats

Apollo Player recognizes these file types:

- MP3 (`.mp3`)
- WAV (`.wav`)

## Music Library

Apollo Player uses the current user's Windows Music folder as its music library. The application reads supported audio files from the top level of this folder when it starts.

The **Import** button copies selected MP3 and WAV files into the Windows Music folder. If a file with the same name already exists, the application asks for permission before it replaces the file.

> [!WARNING]
> The **Remove** button deletes the selected audio file from the Windows Music folder. It does not only remove the track from the displayed list. The application does not move the deleted file to the Recycle Bin.

Apollo Player does not scan subfolders.

## Requirements

To build and run Apollo Player from source, you need:

- A Windows operating system
- The [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- Git
- Visual Studio 2022 with the **.NET desktop development** workload, or the .NET command-line interface

## Install and Run

Prebuilt Windows installers are available in the [`Apollo Player Setup, ReadMe, Icon`](https://github.com/mcnylo/apolloplayer/tree/master/Apollo%20Player%20Setup%2C%20ReadMe%2C%20Icon) folder.

1. Open the installer folder.
2. Select an `.msi` installer.
3. Download the installer.
4. Run the downloaded file.
5. Follow the instructions in the installation wizard.
6. Open Apollo Player after the installation is complete.

## Usage

1. Put MP3 or WAV files in your Windows Music folder, or select **Import** in Apollo Player.
2. Select a track from the music list.
3. Select **Play**.
4. Use the playback controls to pause, stop, seek, or change tracks.
5. Enable shuffle or repeat when required.
6. Use the volume control to adjust or mute the audio.

If you select **Play** without selecting a track, Apollo Player starts the first track in the music list.

## Technology

| Technology | Purpose |
| --- | --- |
| C# | Application logic |
| .NET 8 | Application runtime and build platform |
| WPF | Desktop interface |
| XAML | Interface layout and control styles |
| [NAudio 2.2.1](https://github.com/naudio/NAudio) | Audio file reading and playback |
| [XamlAnimatedGif 2.2.3](https://github.com/XamlAnimatedGif/XamlAnimatedGif) | GIF animation in the WPF interface |

## Version History

### 1.1.07

- Corrected a freeze that could occur after extended playback.
- Updated the initial volume behavior.
- Adjusted long track-name formatting.
- Embedded the music-list font for use on other computers.

### 1.1.06

- Prevented an error when the pause button is selected without an active track.
- Added a custom scrollbar to the music list.
- Added scrolling text for the current track name.
- Shortened long names in the music list with an ellipsis.

### 1.0.05

- Prevented an error when playback resumes after a pause.

### 1.0.04

- Prevented overlapping playback when no track is selected.

### 1.0.03

- Prevented an error when the active track is deleted.

### 1.0.02

- Changed the library location to the Windows Music folder.
- Corrected automatic playback of the next track.

### 1.0.01

- Prevented a freeze when the play button is selected twice.

### 1.0.00

- Created the initial release.

## Acknowledgments

- [NAudio](https://github.com/naudio/NAudio) provides audio reading and playback support.
- The current-track marquee was adapted from [Razan Paul's Silverlight marquee example](https://asp-blogs.azurewebsites.net/razan/a-simple-text-marquee-control-in-silverlight).
