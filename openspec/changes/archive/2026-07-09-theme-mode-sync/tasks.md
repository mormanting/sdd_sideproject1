## 1. Theme State

- [x] 1.1 Add the theme toggle control to the top navigation bar with Light / Dark affordance
- [x] 1.2 Introduce `localStorage.theme` read/write helpers and initialize the page theme from stored preference or Light Mode default
- [x] 1.3 Apply the `.dark` class to `<html>` and wire the shared theme state into the page bootstrap path

## 2. Visual Assets

- [x] 2.1 Add an `id` to the Highlight.js stylesheet link so the code theme can be swapped at runtime
- [x] 2.2 Add the 150ms color transition classes to theme-sensitive surfaces so theme changes animate smoothly
- [x] 2.3 Update the theme-sensitive Tailwind classes for the shell, toolbar, footer, and workspaces so Light and Dark Mode states are visually distinct

## 3. Rendering Linkage

- [x] 3.1 Switch the Highlight.js stylesheet between `github.css` and `github-dark.css` when the theme changes
- [x] 3.2 Reinitialize Mermaid with the active theme and rerender the current preview content after each theme switch
- [x] 3.3 Ensure existing Mermaid diagrams are cleared and regenerated so chart colors stay readable in both themes

## 4. Verification

- [x] 4.1 Test theme persistence across reloads and confirm the stored theme wins over the default
- [x] 4.2 Verify Highlight.js code blocks and Mermaid diagrams remain legible after repeated theme toggles
- [x] 4.3 Check that the UI still falls back to Light Mode when persistence data is unavailable
