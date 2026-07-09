## 1. Language Core

- [x] 1.1 Add the `i18nDictionary` structure with Traditional Chinese and English entries for all required UI text
- [x] 1.2 Implement `localStorage.lang` read/write helpers and initialize the active language from storage or Traditional Chinese by default
- [x] 1.3 Add the language selector to the top navigation bar beside the existing theme toggle

## 2. Data-Driven Markup

- [x] 2.1 Mark all translatable elements with `data-i18n` keys and remove hard-coded visible text from HTML
- [x] 2.2 Add dictionary-backed rendering for the brand, top navigation labels, toolbar labels, footer labels, theme helper text, and slider descriptions
- [x] 2.3 Add translation coverage for Mermaid error messages and any other system copy surfaced in the MVP

## 3. Translation Runtime

- [x] 3.1 Build a DOM translation pass that scans `data-i18n` nodes and injects the active language strings
- [x] 3.2 Provide safe fallback behavior for missing translation keys so the default language remains readable
- [x] 3.3 Wire the language selector to update the UI immediately without page reload and keep the current theme/render state intact

## 4. Verification

- [x] 4.1 Test that switching between Traditional Chinese and English updates all visible labels in place
- [x] 4.2 Verify `localStorage.lang` persists across reloads and wins over the default language
- [x] 4.3 Confirm the UI still renders readable fallback text when a translation key is absent
