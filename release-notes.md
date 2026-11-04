# Changelog

## [0.15.0] - 2026-11-04

- Deleting a parent from the tree now also deletes the descendants that have no
  other live parent, in one undo step. When several Items go, a confirmation
  lists them; it also warns when Views rooted in them are deleted too.
- The properties pane's Delete item still deletes only that Item; its children
  are promoted to the Forest.
- Non-root tree rows now offer Remove from here, which removes one placement
  without deleting the Item.

## [0.14.0] - 2026-11-04

- A write can no longer change a variable's type: the editor offers only the
  variable's own type and the operators it supports, and the engine enforces
  the same rule for synced and MCP changes.
- A write whose target Item was deleted no longer keeps its variable in the
  computed values; the stale write is flagged in the properties pane so it can
  be removed.
- The editor now shows the next sibling at the end of the body, for quick
  navigation without going back to the tree.
- Japanese text on the web uses Noto Sans JP glyphs instead of the browser's
  Chinese fallback.

## [0.13.0] - 2026-11-04

- An empty vault now opens on the tree pane, so the create action is the first
  thing visible.
- The web tree pane links to the published ZapStore listing.
- Android downloads are now split per ABI (arm64-v8a, armeabi-v7a, x86_64), so
  the download is smaller.

## [0.12.0] - 2026-11-04

First public Android release.

- A local-first, structured editor for worldbuilding and narrative work:
  Items form one graph and Tree Views are saved starting points.
- End-to-end encrypted QR sync between devices.
- A local MCP bridge for agent integrations from the web app.
- New launcher icons (adaptive, monochrome and round), a branded Android 12
  splash, and a muted brand loader on the web.
- The web tree pane links to this Android app.
