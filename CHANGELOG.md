# Changelog

Versions match `CFBundleShortVersionString`; `./release.sh <version> "notes"` publishes.

## 1.1.1 — 2026-10-14

- New update-signing key. Copies on 1.0.0 or 1.1.0 can't install updates automatically
  any more: they show "a new version is available" with a link — install this DMG once,
  and automatic updates work again from here on.

## 1.1.0 — 2026-10-14

- **Secrets**: a lock pill after the filters opens a password vault. Add one with
  *New Secret…* or right-click a clip › *Save as Secret…* (the clip leaves the history).
  Values live in the login Keychain, never in history.json, and are never shown; a click
  or ↩ asks for Touch ID (or the Mac password), copies the value marked as concealed so
  other clipboard tools skip it, and wipes the clipboard after 30 s unless you copied
  something else. Delete asks for Touch ID too.
- **Look** tab: 15 menu-bar icons, *Hide the icon* (only with a Summon shortcut; opening
  the app again also shows the panel), 9 accent colours, Compact/Regular/Tall height,
  and where the shortcut opens the panel (top right, at the pointer, screen centre).

- **Keyboard control of the panel**: ↑↓ (⌥ for ×5, ⌃N/⌃P too) move a highlight that
  every open resets to the newest clip; ↩ copies (or pastes, per Settings) and ⌥↩ does
  the other; ⌘1–9 pick the first nine rows, with the numbers shown while ⌘ is held;
  Space opens Quick Look; ⇥/⇧⇥ cycle the filter; ⌘P pins; ⌘⌫ deletes; ⌘, opens
  Settings; Esc closes Quick Look, then leaves Settings, then clears the search, then
  closes. A list scrolling under a resting mouse no longer steals the highlight.
- **Readable on light backgrounds**: denser glass and brighter secondary text; the
  Quick Look popover is dark instead of light-on-light.
- **Passwords are skipped**: copies marked concealed/transient by password managers
  are never recorded (Settings › History › Privacy to turn off).
- **History size**: keep 100, 250, 500 or 1000 unpinned clips. *Clear all* asks for a
  second click.
- Search matches every word in any order ("swift guide" finds "swift language guide").
- The panel drops in and fades from the menu bar, rows follow; it fades out on close.
  Reduce Motion makes both instant.
- Settings tabs use the same sliding pill as the filter and crossfade; the panel
  remembers the last tab. *In the panel* lists every key.
- About: *What's New* and *Report a Problem…* (a pre-filled GitHub issue with version,
  macOS and chip only).
- Right-click menu has *Paste* next to *Copy*; hand cursor on clickable controls;
  VoiceOver labels and actions (pin, delete) on rows.
- Image rows decode once and are cached; history writes are serialised.
- `run-tests.sh` (29 checks); `PASTEBOARD_ARCHES`, `PASTEBOARD_DEBUG` build knobs.

## 1.0.0

- First release: menu-bar history, search, kind filter, day jump, pins, paste stack,
  text transforms, plain-text paste, Quick Look, Sparkle updates.
