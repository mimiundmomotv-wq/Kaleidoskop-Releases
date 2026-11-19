# Installing Kaleidoskop – step by step

This guide is for everyone, no prior knowledge needed. Pick your device:

- [Android phone or tablet](#android)
- [Linux computer](#linux)
- [Any computer with a web browser (no installation)](#web-browser)

All files are on the [Releases](https://github.com/mimiundmomotv-wq/kaleidoskop/releases) page of this repository. Under the newest release, open
**Assets** to see the downloads. The on-screen texts of the app are in German.

---

## Android

> [!WARNING]
> **This app has not been security-checked.** It does not come from the Google Play Store, so it has not
> gone through Google's review, and no independent security audit has been done. It was created with
> substantial help from an AI and is offered as it is, without any guarantee – see [LICENSE](../LICENSE).
> Install it only if you accept that risk, and only from the
> [Releases](https://github.com/mimiundmomotv-wq/kaleidoskop/releases) page of this repository, never from other websites.
>
> To install it, Android must be allowed to install apps from outside the Play Store ("unknown sources").
> Allow this only for as long as you need it, and switch it off again afterwards (step 5).

**What you need:** Android 8 or newer (practically every phone since 2018), about 250 MB of free space.

### Step 1 – Download the APK

1. Open this repository's [Releases](https://github.com/mimiundmomotv-wq/kaleidoskop/releases) page **on your phone**, in a browser such as
   Chrome, Firefox or Samsung Internet.
2. Under the newest release, tap **Assets**, then tap the file ending in **`-android.apk`**
   (for example `kaleidoskop-v1.18-android.apk`).
3. The browser may warn that "this type of file can harm your device". Tap **Download anyway**
   (wording differs between browsers).

The file is now in the **Download** folder of your phone.

### Step 2 – Open the APK

You can open it in one of two ways:

- **From the browser:** tap **Open** in the download message, or open the browser's list of downloads and
  tap the file.
- **From the file manager:** open the app called **Files**, **My Files** or **Eigene Dateien**
  (on Samsung phones), go to **Downloads**, and tap the file.

### Step 3 – Allow installing from this app ("unknown sources")

The first time, Android stops and shows a message such as *"For your security, your phone is currently not
allowed to install unknown apps from this source."* This is expected.

1. Tap **Settings** in that message.
2. Switch on **Allow from this source**.
3. Go back (back gesture or back button).

Android asks this **separately for each app** you install from: if you opened the APK from the browser,
you allow the browser; if you opened it from **Files / My Files / Eigene Dateien**, you allow that file
manager. Only allow the one you actually use.

<details>
<summary>The message did not appear, or you want to set it by hand</summary>

The setting is in a slightly different place depending on the phone. Look for **Install unknown apps**:

- **Google Pixel and most phones:** Settings → Apps → Special app access → **Install unknown apps** →
  choose your browser or Files app → switch on **Allow from this source**.
- **Samsung:** Settings → Apps → ⋮ (top right) → Special access → **Install unknown apps** →
  choose your browser or **My Files / Eigene Dateien** → switch on **Allow from this source**.
- **Xiaomi, Redmi, POCO:** Settings → Privacy protection (or Apps → Manage apps) → Special permissions →
  **Install unknown apps** → choose the app → switch it on.
- If you cannot find it: open Settings and search for **unknown**.
</details>

### Step 4 – Install

1. Tap **Install**.
2. **Google Play Protect** may show a warning such as *"Unsafe app blocked"* or *"App scan recommended"*,
   because it does not know this app. This is the security warning from above. If you still want to
   install, tap **More details** → **Install anyway**, or **Scan app** and then **Install** if the scan
   finds nothing.
3. When it is done, tap **Open**.

On first start, the app asks for access to the **microphone**. It uses it only to react to music while the
app is open; nothing is recorded or sent anywhere. If you decline, everything works except the music effects.

### Step 5 – Switch "unknown sources" off again (recommended)

Go back to **Install unknown apps** (see the box in step 3), choose the browser or file manager you
allowed, and switch **Allow from this source** off again. The installed Kaleidoskop keeps working.

### Updating

Download the newer APK and install it the same way; your settings are kept. If Android says the app
"could not be installed" or that the package "conflicts with an existing package", uninstall the old
version first (long-press the app icon → **Uninstall**) and install again.

### Uninstalling

Long-press the Kaleidoskop icon → **Uninstall** (or Settings → Apps → Kaleidoskop → Uninstall).

---

## Linux

**What you need:** a 64-bit PC (x86-64) with a current Linux (Ubuntu 20.04 or newer, Debian 11+, Fedora,
Arch, …) and graphics with Vulkan or OpenGL 3.3 drivers – any reasonably current Intel, AMD or NVIDIA graphics.

### Step 1 – Download

On the [Releases](https://github.com/mimiundmomotv-wq/kaleidoskop/releases) page, under **Assets**, download the file ending in
**`-linux-x86_64.tar.gz`**. It usually lands in your **Downloads** folder.

### Step 2 – Unpack and install

Open a terminal (in most desktops: press **Ctrl + Alt + T**, or search for "Terminal") and enter these
lines one after another, each followed by **Enter**. Replace `1.18` with the version you downloaded.

```
cd ~/Downloads
tar xzf kaleidoskop-v1.18-linux-x86_64.tar.gz
cd kaleidoskop-v1.18
./install.sh
```

No administrator password is needed; everything is installed only for your user.

### Step 3 – Start

- From the start menu: search for **Kaleidoskop**.
- Or in the terminal: `kaleidoskop` (graphical app) or `kaleidoskop-term` (terminal version).

Press **H** to show or hide the menu, **Q** to quit. All keys are listed in the `README.md` inside the
unpacked folder.

### Optional: music reaction and video recording

- To let Kaleidoskop react to the music you play, it needs the program `parec`. On Ubuntu and Debian:
  `sudo apt install pulseaudio-utils` (on systems with PipeWire, `pipewire-pulse` provides it too).
- To record videos with **R**, install `ffmpeg`: `sudo apt install ffmpeg`.

### Uninstalling

```
~/.local/share/kaleidoskop/uninstall.sh          # keeps your settings
~/.local/share/kaleidoskop/uninstall.sh --all    # also removes your settings
```

---

## Web browser

No installation needed, on any computer with a current browser (Firefox, Chrome, Edge, Safari):

1. On the [Releases](https://github.com/mimiundmomotv-wq/kaleidoskop/releases) page, under **Assets**, download the file ending in **`.html`**.
2. Open it: double-click the downloaded file, or drag it into a browser window.

The browser version is simpler than the apps (no music reaction) and loads nothing from the internet.
