# Glass Player (desktop)

A glass-themed music player in a Tauri shell. Tauri uses your system's built-in
web view instead of bundling a browser, so the installer is a few MB and the
app typically idles at roughly 30 to 70 MB of RAM (Electron apps start around
150 MB or more).

## Option A: build on your machine

You need Node 18+ and Rust (https://rustup.rs). On Linux also install:
`libwebkit2gtk-4.1-dev libgtk-3-dev librsvg2-dev libayatana-appindicator3-dev`
plus `gstreamer1.0-plugins-good gstreamer1.0-libav` (needed for audio).
On Windows you also need the Microsoft C++ Build Tools (WebView2 ships with Windows 11).

    npm install
    npx tauri icon app-icon.png     # generates src-tauri/icons
    npm run dev                     # run it
    npm run build                   # make an installer

The installer ends up in `src-tauri/target/release/bundle/`.

## Option B: let GitHub build it

Push this folder to a GitHub repo, open the Actions tab, and run "build".
It produces Windows, macOS and Linux installers as downloadable artifacts,
with nothing to install locally.

## Editing

The whole UI is `src/index.html`. Change it and re-run.
