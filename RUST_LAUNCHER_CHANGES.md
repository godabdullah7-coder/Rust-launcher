# Rust Launcher changes (on top of Starling 0.8.0)

- App name: `RUST LAUNCHER` (packaging/android/build_apk.py, LABEL)
- Icon: packaging/icons/rust/*.png (all densities), used by build_apk.py
- Controls import: `.rcontrols` or controls `.json` opened from ZArchiver / any file manager
  (manifest filters) or picked with the new **Import** button -> crates/horizon-client/src/import.rs
  (`Kind::Controls`) installs it as a new preset in controls/<mcpe|goycontrol>/
- Controls export: **Exp** button on each preset row writes
  Starling/controls-export/<name>-<system>.rcontrols (crates/horizon-client/src/android_control_ui.rs)
- Where: H > Controls > Presets (the presets modal)
