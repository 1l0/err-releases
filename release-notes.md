# Changelog

## [0.19.3] - 2026-11-13

- Wide layout: the header now sits above the editor pane only. The tree and
  properties panes reach the top of the window and the header no longer spans
  the whole screen.
- The tree's view selector shows the Forest as a forest icon.
- Backlinks: the sort button's arrow now points the way the list is ordered,
  and the redundant per-row arrow is gone.

## [0.19.2] - 2026-11-13

- Android: the store listing's camera disclosure is now visible to ZapStore's
  privacy analysis. No app behavior changed.

## [0.19.1] - 2026-11-13

- Android: the store listing now explains that camera access is only for
  scanning a pairing QR code, and that the QR scanner uses ML Kit. No app
  behavior changed.

## [0.19.0] - 2026-11-13

- The bottom of the editor now shows backlinks: every Item whose body links to
  the current Item, with a count, clickable source rows, and nearest/farthest
  tree-distance sorting.
- Selecting an Item from a link, search or backlink expands collapsed ancestors
  and centers the row in the tree.
- Collapsed tree branches are remembered per device across restarts.
- Web: the Install Android App link moved from the tree pane to the bottom of
  the properties pane.

## [0.18.0] - 2026-11-09

- The editor footer now shows a character count instead of a word count.
- Large vaults load, expand and search much faster: a reload no longer reads
  every note body, tree levels load in one request, and search runs in the
  engine with a short snippet around the match.
- Web: the OPFS storage-usage repair no longer leaves DevTools reporting an
  enormous size, and release builds log when a repair runs.

## [0.17.0] - 2026-11-07

- The body editor starts at one line when empty and grows as you type, instead
  of always reserving ten lines.
- A word count appears below the body, aligned with the right edge of the
  editor. It is hidden for an empty body and in preview.
- Link and variable suggestions stay tappable when the body is short, and the
  caret keeps its line while the suggestion card is open.

## [0.16.0] - 2026-11-06

- Web builds ask the browser for persistent storage and warn in the header when
  the vault can be evicted, with a one-click install prompt where available.
- Phone-sized web browsers now start QR sync on the show/scan choice, and can
  scan another device's code without first creating a room.
- Search results can be driven from the keyboard: Down/Up move the highlighted
  row, Enter opens it and Esc closes the search.
- The editor's [[link]] and {{variable}} suggestions follow the caret line, and
  Esc cancels the open construct. Japanese IME candidates now stay by the
  caret on the web.
- A light swipe turns the page in the narrow layout.
- iOS: creating an Item focuses its title immediately, and search input is
  fixed.

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
