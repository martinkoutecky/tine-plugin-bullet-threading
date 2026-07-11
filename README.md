# Bullet threading for Tine

An intentionally tiny community plugin: enabling it activates Tine's constrained
`thread-lines` decoration. Tine draws the connectors; the plugin cannot inject CSS,
run browser code, or touch graph data.

Build with `cargo build --release`, then run Tine's `plugin:check` command on this
directory. Licensed MIT. AI-primary development, reviewed and published by Martin
Koutecký.
