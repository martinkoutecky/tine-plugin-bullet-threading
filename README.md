# Bullet threading for Tine

Draw subtle elbow connectors from parent bullets to their children, making
nested outlines easier to follow.

![Bullet threading enabled in Tine](docs/bullet-threading.png)

## How to use it

Install **Bullet threading** from **Settings → Plugins**, then enable its toggle.
The connectors appear immediately throughout the outline. Open the plugin's
Settings page to choose all nested outlines or only the focused block's ancestry,
and to choose subtle or standard connector strength. Disable or uninstall
the plugin to return to Tine's normal bullet guides; your notes are never
changed.

## Safety model

This is a behavioral port of Peng Xiao's MIT-licensed Logseq Plugin Bullet
Threading, pinned to the source revision recorded in `manifest.json`. It is a
declarative visual plugin: it requests Tine's built-in
`thread-lines` decoration, and Tine draws the connectors. The plugin cannot
inject CSS, run browser code, access files or the network, or read or write graph
data. Tine applies these two host-rendered settings directly; the guest receives
activation/settings events but no block snapshots and returns no effects.

## Development

Build with `cargo build --release`, then run Tine's `plugin:check` command on
this directory. Licensed MIT. AI-primary development, reviewed and published by
Martin Koutecký.
