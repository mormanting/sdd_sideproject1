## ADDED Requirements

### Requirement: Default light-mode Traditional Chinese shell
The system MUST default to Light Mode, use Traditional Chinese for visible UI text, and apply monospace typography to the editor shell.

#### Scenario: Initial page load uses the default shell
- **WHEN** the page is opened for the first time
- **THEN** the interface SHALL render in Light Mode with Traditional Chinese labels and monospace text styling

### Requirement: Desktop dual-pane and mobile toggle layout
The system MUST render a top navigation bar, a toolbar, a main workspace, and a footer; on screens at or above 768px wide, the workspace MUST present editor and preview panes side by side at equal width, and on screens below 768px wide, the workspace MUST switch to a single-pane mode with explicit editor/preview switching controls.

#### Scenario: Desktop viewport shows two panes
- **WHEN** the viewport width is 768px or greater
- **THEN** the editor pane and preview pane SHALL each occupy 50% of the workspace width

#### Scenario: Mobile viewport requires explicit switching
- **WHEN** the viewport width is below 768px
- **THEN** the interface SHALL show a single active pane and provide controls to switch between editing and previewing

### Requirement: Toolbar inserts Markdown syntax at the cursor
The system MUST insert the selected Markdown syntax into the editor at the current cursor position when a toolbar button is activated.

#### Scenario: User inserts bold syntax
- **WHEN** the user activates the bold toolbar button
- **THEN** the editor SHALL insert bold Markdown syntax at the cursor position

### Requirement: Footer shows live text statistics
The system MUST show live character count and word count in the footer, and the character count MUST include punctuation marks.

#### Scenario: Statistics update after editing
- **WHEN** the editor content changes
- **THEN** the footer SHALL update the character count and word count without requiring a page refresh

### Requirement: Footer font-size control applies to editor and preview
The system MUST provide a font-size slider in the footer with a range from 12px to 24px, defaulting to 16px, and changes MUST apply immediately to both the editor and the preview.

#### Scenario: User changes the font size
- **WHEN** the user moves the font-size slider
- **THEN** the editor and preview text SHALL update to the selected size within the allowed range
