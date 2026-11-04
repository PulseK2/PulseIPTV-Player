<div align="center">

  <img width="2752" height="1536" alt="PULSEIPTV" src="https://github.com/user-attachments/assets/3e566f80-6a45-43eb-b6a3-0e54b4eee650" />
<h1>⚡ PULSE IPTV</h1>
  <p><strong>Next-Generation, Hardware-Accelerated IPTV Desktop Player for Windows</strong></p>

  <p>
    <a href="#-key-features">Features</a> •
    <a href="#-quick-start">Quick Start</a> •
    <a href="#-keyboard-shortcuts">Shortcuts</a> •
    <a href="#-architecture">Architecture</a> •
    <a href="#-building-from-source">Build</a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011%20(64--bit)-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Platform" />
    <img src="https://img.shields.io/badge/.NET-10.0%20WPF-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET 10" />
    <img src="https://img.shields.io/badge/Core-LibVLC%20Direct3D11-FF8800?style=for-the-badge&logo=vlcmediaplayer&logoColor=white" alt="LibVLC Direct3D11" />
    <img src="https://img.shields.io/badge/Playback-4K%20UHD%20%7C%20HDR-00E5FF?style=for-the-badge" alt="4K HDR" />
    <img src="https://img.shields.io/badge/API-Xtream%20Codes%20%26%20M3U-10B981?style=for-the-badge" alt="Xtream Codes & M3U" />
  </p>

</div>

---

> **Say goodbye to sluggish channels and constant buffering.**  
> Pulse IPTV is an ultra-fast, modern desktop player built specifically for iptv streaming. Powered by native **LibVLC Direct3D11 hardware decoding**, Pulse IPTV provides silky-smooth 4K 60fps playback, instant channel zapping, full offline EPG guides, TV series browsing, and intelligent multi-server failover.

---

## ✨ Why Pulse IPTV?

<table>
  <tr>
    <td width="50%">
      <h3>⚡ Instant Hardware Decoding</h3>
      <p>Direct3D11 GPU acceleration offloads decoding directly to your graphics card (NVIDIA, AMD, Intel). Smoothly streams 4K UHD, 60fps sports, and Rec.2020 HDR with zero frame drops.</p>
    </td>
    <td width="50%">
      <h3>📺 Zero-Lag Channel Zapping</h3>
      <p>Seamlessly toggle between ultra-low-latency <b>MPEG-TS (<code>.ts</code>)</b> for sub-second live channel switching and adaptive bitrate <b>HLS (<code>.m3u8</code>)</b> with one click.</p>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3>🛡️ Bulletproof Server Failover</h3>
      <p>Connect primary and backup server URLs. If your IPTV provider's upstream CDN encounters a 502/down state, Pulse IPTV switches servers automatically in the background.</p>
    </td>
    <td width="50%">
      <h3>📅 Lightning-Fast EPG Schedules</h3>
      <p>Gzip-compressed local caching saves XMLTV program guides so you never wait for 10,000+ channel schedules to redownload on launch. Includes in-player timeline progress bars.</p>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3>🎬 Cinema & TV Series Hub</h3>
      <p>Full on-demand library with poster artwork, release dates, plot summaries, season pickers, and episode descriptions. Precise time scrubbing for movies and episodes.</p>
    </td>
    <td width="50%">
      <h3>📥 Offline Video Downloads</h3>
      <p>Built-in background download manager. Save full movies and TV episodes directly to your local PC for travel or offline entertainment with real-time speed tracking.</p>
    </td>
  </tr>
</table>

---

## 🌟 Key Features

### 🔌 Xtream Codes & Playlist Support
- **Universal Input Parser**: Paste any Xtream Codes URL, raw M3U link, or credentials—our parser automatically extracts server host, port, username, and password.
- **Multi-Account Profile Manager**: Switch between multiple IPTV provider subscriptions in seconds.
- **Offline & Demo Mode**: Built-in verified public HD streams (NASA TV, Bloomberg Markets, France 24, DW News, Nature 4K) so you can test and explore immediately without an account.
- **Local M3U Playlists**: Drag and drop or open `.m3u` and `.m3u8` playlist files.

### 🎨 Fluent Dark UI & Virtualized Search
- **Instant Search Virtualization**: Filter across 50,000+ live channels, movies, and shows with 60fps buttery responsiveness.
- **One-Click Favorites**: Star your top channels and movies to keep them instantly accessible.
- **Aspect Ratio Cycling**: Switch between Default, 16:9, 4:3, and 21:9 UltraWide on the fly.
- **Immersive Fullscreen**: Double-click or press `F11` / `Escape` for true distraction-free playback.

---

## 🚀 Quick Start (Portable Release)

No installation or prerequisites required! The release package is **100% self-contained**:

1. Download the latest **`PulseIPTV_v1.0_Windows_x64.zip`** from the [Releases](dist/) folder.
2. Extract the archive to any folder on your PC.
3. Double-click **`PulseIPTV.exe`** to launch.
4. Click **`⚡ Connect Xtream Codes`** or **`🌍 Explore Demo Streams`** to start watching!

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|:---|:---|
| <kbd>Space</kbd> | Toggle Play / Pause |
| <kbd>F11</kbd> or **Double-Click** | Toggle True Theater Fullscreen |
| <kbd>Escape</kbd> | Exit Fullscreen Mode |
| <kbd>↑</kbd> / <kbd>↓</kbd> | Zapping: Next / Previous Channel |
| <kbd>M</kbd> | Mute / Unmute Audio |

---

## 🛠️ Building From Source

### Prerequisites
- Windows 10 (Build 19041+) or Windows 11 (64-bit)
- [.NET 10.0 SDK](https://dotnet.microsoft.com/download)

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/PulseIPTV.git
cd PulseIPTV
```

### 2. Run with Developer Launcher
```cmd
run.bat
```
*`run.bat` unblocks binaries, cleans old build artifacts, compiles the latest source code, and launches the application.*

### 3. Or Publish Standalone Release
```powershell
dotnet publish PulseIPTV.csproj -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -o dist/PulseIPTV
```

---

## 📁 Architecture Overview

```
PulseIPTV/
├── Models/
│   └── XtreamModels.cs        # Xtream API schemas, EPG items, Accounts, and Stream contracts
├── Services/
│   ├── VlcPlayerService.cs    # Native LibVLC engine, Direct3D11 pipeline, event dispatching
│   ├── XtreamService.cs       # Async HTTP client, URL parser, failover logic, EPG gzip caching
│   ├── StorageService.cs      # Local encrypted app state, favorites, and account store
│   └── DownloadService.cs     # Background file downloader with progress reporting
├── ViewModels/
│   └── MainViewModel.cs       # Reactive MVVM orchestrator, UI virtualization filters
├── Converters/                # WPF XAML value converters (Visibility, Aspect, Color)
├── MainWindow.xaml            # Modern Fluent UI shell, OSD overlays, VideoView surface
├── App.xaml                   # Design tokens, color brushes, global exception hooks
└── PulseIPTV.csproj           # .NET 10 project definition & LibVLC target orchestrator
```

---

## 🔒 Privacy & Security

- **Zero Telemetry**: Pulse IPTV does not track, store, or transmit your streaming habits or credentials.
- **Direct Connection**: All stream data flows strictly between your computer and your IPTV provider's servers.
- **Local Persistence**: Accounts, favorites, and settings are saved locally in your Windows `%APPDATA%\PulseIPTV` folder.

---

## ⭐ Support & Community

If you find Pulse IPTV helpful, please consider **starring the repository** ⭐ to support continuous development!

Have a question, suggestion, or bug report? Feel free to open an [Issue](issues) or submit a [Pull Request](pulls).

---

<div align="center">
  <sub>Built with ❤️ for high-performance IPTV streaming. Distributed under the MIT License.</sub>
</div>
