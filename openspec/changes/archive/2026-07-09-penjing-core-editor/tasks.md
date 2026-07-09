## 1. Entry Shell

- [x] 1.1 Create the single-file `index.html` entry with the required CDN imports and default Light Mode / Traditional Chinese bootstrap state
- [x] 1.2 Build the fixed top navigation bar, toolbar, main workspace, and footer layout with monospace styling and 4px corner radius
- [x] 1.3 Add the responsive workspace behavior so desktop shows split panes and mobile switches to a single active pane with explicit editor/preview toggles

## 2. Editor Interactions

- [x] 2.1 Implement toolbar actions that insert Markdown syntax at the current cursor position in the textarea editor
- [x] 2.2 Add footer character and word statistics that update live as the editor content changes
- [x] 2.3 Implement the footer font-size slider with a 12px to 24px range and immediate application to both editor and preview

## 3. Markdown Rendering

- [x] 3.1 Configure the Markdown parsing pipeline for headings, bold, italic, lists, and links using `marked`
- [x] 3.2 Integrate `highlight.js` and `marked-highlight` so fenced JSON and YAML blocks render with syntax highlighting and preserved structure
- [x] 3.3 Add Gherkin / Cucumber language support so Feature, Scenario, Given, When, and Then lines receive distinct highlighting
- [x] 3.4 Detect fenced Mermaid blocks, convert them into Mermaid containers, and render them as SVG diagrams in the preview
- [x] 3.5 Add a 300ms debounce around Mermaid re-rendering so diagram redraws only occur after typing stops

## 4. Verification

- [x] 4.1 Smoke-test the shell, insertion, statistics, font scaling, and responsive toggle behavior with representative sample content
- [x] 4.2 Validate the preview output for Markdown, code highlighting, Gherkin, and Mermaid cases against the defined specs
