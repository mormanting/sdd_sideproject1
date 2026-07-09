## ADDED Requirements

### Requirement: Highlight.js stylesheet swaps with theme
The system MUST dynamically enable the appropriate Highlight.js stylesheet for the active theme, using `github.css` for Light Mode and `github-dark.css` for Dark Mode.

#### Scenario: Light theme selects the light code style
- **WHEN** the active theme is Light Mode
- **THEN** the preview SHALL use the Highlight.js stylesheet for `github.css`

#### Scenario: Dark theme selects the dark code style
- **WHEN** the active theme is Dark Mode
- **THEN** the preview SHALL use the Highlight.js stylesheet for `github-dark.css`

### Requirement: Mermaid theme reinitializes on theme change
The system MUST reinitialize Mermaid with `theme: 'default'` in Light Mode and `theme: 'dark'` in Dark Mode whenever the theme changes.

#### Scenario: Dark mode reinitializes Mermaid
- **WHEN** the user switches to Dark Mode
- **THEN** Mermaid SHALL be reinitialized with the dark theme before rendering diagrams

#### Scenario: Light mode reinitializes Mermaid
- **WHEN** the user switches back to Light Mode
- **THEN** Mermaid SHALL be reinitialized with the default theme before rendering diagrams

### Requirement: Mermaid diagrams rerender after theme changes
The system MUST reparse the current editor content and rerender all Mermaid diagrams after a theme change so diagram text and lines remain readable in the active theme.

#### Scenario: Theme change updates existing diagrams
- **WHEN** the theme is changed while Mermaid diagrams are already visible
- **THEN** the system SHALL rerender the current diagrams using the new theme settings

