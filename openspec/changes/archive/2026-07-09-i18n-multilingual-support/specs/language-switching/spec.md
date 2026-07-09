## ADDED Requirements

### Requirement: Language selector and persistence
The system MUST provide a language selector in the top navigation bar, persist the selected language in `localStorage.lang`, and initialize the page using the saved language when available or Traditional Chinese otherwise.

#### Scenario: Existing language preference is restored
- **WHEN** the page loads and `localStorage.lang` contains a saved language code
- **THEN** the system SHALL apply that language before the UI becomes interactive

#### Scenario: No preference falls back to Traditional Chinese
- **WHEN** the page loads and no saved language code exists
- **THEN** the system SHALL default to Traditional Chinese

### Requirement: Language switching happens without reload
The system MUST update the active language immediately when the user selects a new language and MUST NOT require a page reload.

#### Scenario: User switches to English
- **WHEN** the user selects English from the language selector
- **THEN** the interface SHALL update in place without reloading the page

#### Scenario: User switches back to Traditional Chinese
- **WHEN** the user selects Traditional Chinese from the language selector
- **THEN** the interface SHALL update in place without reloading the page

### Requirement: Supported initial languages are Traditional Chinese and English
The system MUST support Traditional Chinese and English as the initial language set and MUST allow future languages to be added through JavaScript dictionary expansion without changing HTML structure.

#### Scenario: Supported language is selected
- **WHEN** the user selects either Traditional Chinese or English
- **THEN** the system SHALL apply the corresponding language dictionary

#### Scenario: Future language is added through dictionary extension
- **WHEN** a new language dictionary is added in JavaScript
- **THEN** the system SHALL be able to render that language without requiring HTML markup changes

