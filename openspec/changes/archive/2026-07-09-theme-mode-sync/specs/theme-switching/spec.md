## ADDED Requirements

### Requirement: Theme toggle and persistence
The system MUST provide a theme toggle button in the top navigation bar, persist the selected theme in `localStorage.theme`, and initialize the page using the stored theme when available or Light Mode otherwise.

#### Scenario: Existing preference is restored
- **WHEN** the page loads and `localStorage.theme` contains a saved theme value
- **THEN** the system SHALL apply that theme before the UI becomes interactive

#### Scenario: No preference falls back to light mode
- **WHEN** the page loads and no saved theme value exists
- **THEN** the system SHALL default to Light Mode

### Requirement: Root dark class drives the global UI theme
The system MUST apply or remove the `.dark` class on the `<html>` element when the theme changes so that Tailwind dark-mode styles are activated globally.

#### Scenario: User switches to dark mode
- **WHEN** the user activates the theme toggle for Dark Mode
- **THEN** the `<html>` element SHALL include the `.dark` class

#### Scenario: User switches back to light mode
- **WHEN** the user activates the theme toggle for Light Mode
- **THEN** the `<html>` element SHALL not include the `.dark` class

### Requirement: Theme transition remains smooth
The system MUST apply a 150ms color transition to theme-sensitive surfaces so the UI does not flash abruptly during a theme change.

#### Scenario: Theme change animates smoothly
- **WHEN** the theme is changed
- **THEN** the affected UI surfaces SHALL transition their colors over 150ms

