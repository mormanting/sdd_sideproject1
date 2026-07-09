## ADDED Requirements

### Requirement: Basic Markdown rendering
The system MUST render headings H1 through H6, bold text, italic text, unordered lists, ordered lists, and hyperlinks in the preview area.

#### Scenario: Markdown content is rendered as HTML
- **WHEN** the editor contains standard Markdown syntax for headings, emphasis, lists, or links
- **THEN** the preview SHALL render the corresponding HTML presentation

### Requirement: Structured code highlighting for JSON, YAML, and Gherkin
The system MUST detect fenced code blocks labeled JSON, YAML, cucumber, or gherkin and render them with syntax highlighting appropriate to the detected language, including distinct styling for Gherkin keywords such as Feature, Scenario, Given, When, and Then.

#### Scenario: JSON and YAML blocks are highlighted
- **WHEN** the editor contains a fenced code block labeled json or yaml
- **THEN** the preview SHALL preserve structured formatting and apply syntax highlighting

#### Scenario: Gherkin keywords are distinguished
- **WHEN** the editor contains a fenced code block labeled cucumber or gherkin
- **THEN** the preview SHALL highlight behavioral keywords with distinct styles

### Requirement: Mermaid blocks render as vector diagrams
The system MUST detect fenced code blocks labeled mermaid, convert them into Mermaid containers, and render them as SVG diagrams in the preview area.

#### Scenario: Mermaid block renders into SVG
- **WHEN** the editor contains a fenced code block starting with mermaid
- **THEN** the preview SHALL replace the code block with a rendered SVG diagram

### Requirement: Mermaid re-rendering is debounced
The system MUST delay Mermaid re-rendering until the user has stopped typing for at least 300 milliseconds.

#### Scenario: Continuous typing does not trigger repeated redraws
- **WHEN** the user continues typing in the Mermaid block
- **THEN** the system SHALL defer diagram re-rendering until 300 milliseconds of inactivity have elapsed
