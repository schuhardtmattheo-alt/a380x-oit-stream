# A380X OIT Stream – A web browser on your OIT, flyPad and EFB

**Turn the OITs of the FlyByWire A380X and the flyPad of the FlyByWire A320 into tablets – and the EFBs of the Fenix A320.** This mod puts a full web browser on both
Onboard Information Terminals. Watch YouTube, check a flight tracker, read the news or browse your charts
on a long cruise, right inside the cockpit, operated by clicking directly on the OIT.

> Unofficial community mod for **Microsoft Flight Simulator 2020**. Not affiliated with FlyByWire Simulations.

## Features
- 🌐 **Real browser on the OIT:** modern websites and YouTube with sound, powered by the Edge/Chrome engine.
- 🔎 **Finds your tablets automatically:** FBW A380X (OITs + flyPad), FBW A320, Headwind A330, Fenix A319/A320/A321, PMDG 737 and other aircraft with an HTML EFB. The browser adapts to each screen size.
- ⭐ **Bookmarks & SimBrief button:** one tap to SimBrief OFP, YouTube, Flightradar24, Navigraph Charts, METAR/TAF, Windy.
- 🔊 **Volume & mute** right on the tablet.
- ⌨️ **Type with your real keyboard** – click a text field and just type (sim key bindings are paused meanwhile).
- ⬆️ **Auto-update:** the app tells you when a new version is available.
- ✈️ **A380X and A320:** works on both OITs of the A380X on the flyPad (EFB) of the FBW A320 and on both EFBs (captain and FO) of the Fenix A320.
- 👨‍✈️ **Both sides, independent:** the captain and first officer OITs each have their own browser.
- 🖱️ **Use it on the OIT:** click, drag, scroll, address bar, back/forward/reload/home and an on-screen keyboard.
- 🤝 **Shared cockpit sync via invite link:** flying together (e.g. YourControls)? Share a link – no VPN or port forwarding – and TV on/off, pages and YouTube play/pause/position stay in sync for both pilots.
- 🔘 **One-click toggle:** a small **TV** button switches between browser and normal OIT. Videos pause automatically.
- 🪟 **Optional window mirroring:** show any window from your PC on both OITs instead.
- ⚙️ **Adjustable:** 5–30 frames per second and image quality, both changeable live.
- 🧰 **All-in-one app:** install, update, uninstall and start the browser from one window with a clear status overview.
- 🔒 **Private:** the browser and its picture stay on your PC. Shared cockpit only exchanges small sync messages (page address, play/pause, position) with your co-pilot.

## Safe by design
- The aircraft packages (FlyByWire, Fenix) are **never touched**. The mod is a separate package that overlays a single file.
- **No panel.cfg override.**
- **Uninstall** with one click. The app then verifies that the FlyByWire original is intact.
- **FBW updated?** The app detects it and re-applies the mod to the new version with one click.

## Requirements
- Microsoft Flight Simulator 2020 (PC)
- At least one supported aircraft with an HTML tablet/EFB in the Community folder (e.g. FBW A380X/A320, Headwind A330, Fenix, PMDG 737)
- Windows 10/11, 64-bit, with Microsoft Edge (preinstalled) or Google Chrome

## Installation
1. Back up your Community folder (recommended).
2. Close MSFS and run **A380X OIT Stream.exe**.
3. Click **Install**, then **Start stream**.
4. In the cockpit, click **TV** on the OIT (A380X) or on the flyPad/EFB (A320).

Windows SmartScreen may warn because the app is not code-signed: click *More info* → *Run anyway*.

## How it works
MSFS instruments run on an old built-in web engine that cannot play YouTube. The app therefore runs a hidden,
dedicated Edge/Chrome browser for each OIT side. It streams the picture to the OIT and sends your clicks and typing back.

## Known limitations
- If FlyByWire shows its legacy OIT view, it may cover the browser.
- MSFS 2024 is not supported.

## Changelog
**1.7.0:** Automatic tablet detection (Headwind A330, PMDG 737, A380X flyPad, …) and auto-fit to any screen size, bookmarks menu, SimBrief button, volume/mute, real keyboard typing, app auto-update.
**1.6.0:** Fenix A320 support: browser on the captain and FO EFB.
**1.5.0:** FlyByWire A320 support: browser on the flyPad (EFB).
**1.4.0:** New modern app design (CustomTkinter), shared cockpit via Cloudflare invite link.
**1.3.0:** Shared cockpit sync (host/join), auto keyboard on text fields, keyboard position toggle, flicker fix.
**1.1.0:** Built-in browser on both OITs (independent left/right), touch controls, on-screen keyboard.
**1.0.0:** Initial release (window mirroring).

## Download
Get **A380X OIT Stream.exe** from the [latest release](../../releases/latest). Full user guide: [GUIDE.md](GUIDE.md).
