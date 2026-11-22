# A380X OIT Stream – User Guide

Puts a **web browser on both OITs** (captain and first officer) of the FlyByWire A380X and on the **flyPad (EFB)** of the FlyByWire A320 and on both **EFBs of the Fenix A320** in MSFS 2020.
Watch YouTube, browse websites and use them directly on the OIT. You can also mirror any window from your PC instead.
Everything is done with **`A380X OIT Stream.exe`**. You don't need to install anything else.

## Requirements
- Windows 10/11 (64-bit)
- Microsoft Flight Simulator 2020
- At least one of FlyByWire A380X, FlyByWire A320 or Fenix A320 installed in your Community folder
- Microsoft Edge (preinstalled on Windows) or Google Chrome, used for the built-in browser

## 0. Before the first install: make a backup
Copy your whole Community folder somewhere safe.

## 1. Install
1. Close MSFS.
2. Start `A380X OIT Stream.exe`. Everything under **Status** should be green.
   - Windows may show "Windows protected your PC" because the app is not code-signed.
     Click *More info* → *Run anyway*.
3. Click **Install**.

The FlyByWire package is **never modified**. The mod lives in its own folder (`zz-a380x-oit-stream`)
and only overlays the file `oit.html` (A380X) and `efb.html` (FBW A320) and `EfbHost_Captain.html` / `EfbHost_FO.html` (Fenix).

## 2. Use the browser on the OIT
1. In the app, choose Source **"Built-in browser"** (the default) and click **▶ Start stream**.
2. In the A380X, click **TV** in the bottom-right corner of the left or right OIT.
3. The OIT now works like a tablet browser:
   - **Click/tap** on the page to use it. Hold and drag to move sliders such as the YouTube seek bar.
   - **< / >** go back and forward, **Reload** reloads the page, **Home** opens your home page.
   - Click the **address bar** to type an address or a search term – with the on-screen keyboard or simply your **real PC keyboard**
     (while the keyboard panel is open, MSFS key bindings are paused; Enter sends, Esc closes).
   - **Keys** opens the keyboard to type into the page, e.g. the YouTube search box.
   - **Up / Down** or the mouse wheel scroll the page.
   - **SimBrief** opens your latest SimBrief OFP (sign in once via "Show browser on desktop").
   - **Menu** shows bookmarks (YouTube, SimBrief, Flightradar24, Navigraph Charts, METAR/TAF, Windy) and the volume/mute controls.
   - **Exit** returns to the normal OIT/EFB. Videos on that side are paused automatically.
   - **A320:** the **TV** button sits in the bottom-right corner of the flyPad; everything else works the same.
     The flyPad shares the browser of the captain side (left).
   - **Fenix A320:** the **TV** button is in the bottom-right corner of the captain and FO EFB (left/right browser).
4. Each OIT has its **own browser**: the captain and the first officer can watch different things.

The browser runs invisibly in the background; sound plays through your PC as usual.
To sign in to YouTube or other sites with your real keyboard, click **Show browser on desktop**,
sign in there, then click **Hide browser again**. Sign-ins are kept for the next time.

### Shared cockpit (flying together, e.g. with YourControls)
Both pilots install the mod and use the built-in browser. The two apps connect with an **invite link**, and per
OIT side (left/right) they keep **TV on/off, the open page, and video play/pause/position** in sync.
Each PC loads the page itself; no video is sent over the internet. It works over the internet:
no VPN, no port forwarding and no account are needed.

1. **Pilot 1:** open the **Shared cockpit** tab, choose **I host** and click **Create invite link**.
   The first time, the app downloads Cloudflare's official tunnel tool once (~60 MB).
   The link (`https://….trycloudflare.com/…`) is copied automatically. Send it to your co-pilot.
2. **Pilot 2:** choose **I join**, paste the link and click **Join**.
3. Both: start the built-in browser (**Stream** tab → **▶ Start**). Whatever one pilot does on an OIT now happens for both.

The secret part at the end of the link is the key: only someone with the full link can join.
A new link is created every time you host.

Notes: YouTube ads can differ between the two PCs, so videos may run out of sync during ads and re-sync afterwards.
Scrolling and typing are not synced, only the page and video. Window mirroring is not synced.

### Alternative: mirror a window
Choose Source **"Mirror a window"**, select a window and start. Both OITs show that window.
This mode is view-only. Do not minimize the window; it may stay behind MSFS.
If the image is black, set Method to "Screen (window must be visible)".

The **Frames/s** and **Quality** sliders take effect immediately in both modes.

### Supported aircraft
The app finds tablets automatically (status row "Tablets found"): every instrument in a panel.cfg whose path contains
EFB / tablet / flyPad, plus the A380X OITs. Tested layouts: FBW A380X, FBW A320, Headwind A330, Fenix A319/A320/A321, PMDG 737.
Installed a new aircraft? Click **Update** in the Mod tab. The browser adapts to each screen size automatically.

### App updates
If a new version is published, a green **Update to vX** button appears at the top of the app.
After updating, click **Update** in the Mod tab so the cockpit gets the new files too.

## 3. Uninstall
Click **Uninstall & restore original** in the app.
The app removes the mod folder and then verifies that the FlyByWire original file is unmodified (✓).

## 4. After a FlyByWire update
Start the app. If the status says "outdated – FBW was updated", click **Update**.

## Known limitations
- If FBW shows the "legacy" OIT view, it may be drawn on top of the stream.
- Keep an eye on MSFS memory usage during your first long session.

## For developers
Source: `src/OITStream` (instrument, ES5), `companion/oit_browser.py` (built-in browser via the Chrome DevTools Protocol),
`companion/oit_stream.py` (window capture + local server), `tools/build_package.py` (package build, layout.json),
`app/oit_stream_manager.py` (app). Rebuild the exe with `build_exe.bat`.
