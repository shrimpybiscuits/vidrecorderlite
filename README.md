# VidRecorder Lite

A simple camera recorder with numbered takes and a built-in teleprompter. It runs in Chrome or Edge, and you can install it as a desktop app with its own icon.

## What it does

- **Project name** goes at the top. Every recording is named `<Project> - Take 1`, `Take 2`, `Take 3`… Numbering restarts each day and is kept per project, so reloading the app doesn't reset it. Deleted take numbers are never reused, so your notes stay accurate.
- **Record / Stop**: one big button. An optional 3·2·1 countdown is in Settings (⚙).
- **Play / Pause**: plays the selected take, with a scrub bar. Click any take in the **Takes** strip to review it, and click **Back to live** to return to the camera.
- **Save**: opens a "Save as" dialog so you choose the folder. The file name is filled in for you, for example `Spring Promo - Take 3.mp4`. Saved takes show a ✓.
- **Delete**: removes the selected take. It asks you first, and warns you if the take hasn't been saved.
- **Teleprompter** tab: your script scrolls over the live camera. With "Scroll starts with record" on (in Settings), pressing Record starts both the recording and the scroll. Speed, size, mirror, color and font controls all carry over from the original teleprompter.

Takes live in memory until you save them. If you try to close the app with unsaved takes, it warns you first.

## Put it on your desktop as an icon

The app has to be served over `https` once so the browser can install it. After that, it opens from a desktop icon in its own window, with no address bar or commands, and it also works offline.

**1. Turn on GitHub Pages (one time)**
In this repo on GitHub, go to **Settings → Pages**. Under **Build and deployment**, pick **Deploy from a branch**, choose the branch that has these files (e.g. `main`) and the `/ (root)` folder, then click **Save**. About a minute later the page shows your app's address, something like `https://<your-username>.github.io/vidrecorderlite/`.

**2. Install it (one time)**
Open that address in **Chrome** or **Edge**, then:
- **Chrome:** click the install icon (a monitor with a down arrow) at the right end of the address bar, or open **⋮ → Cast, save and share → Install page as app…**.
- **Edge:** open **… → Apps → Install this site as an app**.

Click **Install** and allow camera and microphone access when it asks.

**3. Pin it**
- **Windows:** the app is added to the Start menu. Right-click it to pin it to the taskbar. To get a desktop icon, drag it from the Start menu onto the desktop, or check "Create desktop shortcut" when installing in Edge.
- **Mac:** it appears in your **Applications** folder (Chrome Apps / Edge Apps). Drag it to the Dock.

From then on, just click the icon.

### No-hosting alternative

Download this folder, then double-click `index.html` to open it in Chrome or Edge. To get a desktop icon this way, make a shortcut to `index.html` (Windows: right-click → *Create shortcut*, then drag it to the desktop; Mac: right-click → *Make Alias*). Recording, playback and the "Save as" dialog all work. Only the separate-window app install requires the GitHub Pages route above.

## Browser notes

- **Chrome / Edge (recommended):** full support, including the "Save as" dialog.
- **Safari / Firefox:** recording works, but Save downloads straight to your Downloads folder. To choose a folder each time, turn on "Ask where to save each file" in the browser's download settings.
- Recordings are MP4 where the browser supports it, otherwise WebM.
