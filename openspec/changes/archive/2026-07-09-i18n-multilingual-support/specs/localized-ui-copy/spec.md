## ADDED Requirements

### Requirement: UI text is data-driven
The system MUST source all visible UI text from JavaScript dictionary entries and MUST mark translatable DOM nodes with `data-i18n` keys.

#### Scenario: Top-level UI copy is injected from the dictionary
- **WHEN** the page renders
- **THEN** visible UI text SHALL be populated from the active language dictionary

#### Scenario: A translatable element exposes a key
- **WHEN** an element participates in UI translation
- **THEN** it SHALL expose a `data-i18n` key for script-driven text injection

### Requirement: Translation coverage includes shell, controls, and messages
The system MUST translate the top navigation labels, toolbar labels, footer labels, theme toggle helper text, slider descriptions, and Mermaid error messages.

#### Scenario: Toolbar label changes with language
- **WHEN** the active language changes
- **THEN** toolbar labels SHALL update to the selected language

#### Scenario: Mermaid error text changes with language
- **WHEN** Mermaid reports an incomplete syntax error
- **THEN** the system SHALL display the error message in the active language

### Requirement: Missing translation keys fall back safely
The system MUST fall back to the default language text when a translation key is missing so the UI remains readable.

#### Scenario: A key is missing in the active language
- **WHEN** the active language dictionary does not define a requested key
- **THEN** the system SHALL display the default language value instead of leaving the text blank

### Requirement: No hard-coded visible copy remains in HTML
The system MUST not keep user-visible strings hard-coded in HTML once the localization system is active.

#### Scenario: Localization audit checks the markup
- **WHEN** the localization markup is reviewed
- **THEN** visible text content SHALL be sourced from `data-i18n` keys rather than inline HTML literals

