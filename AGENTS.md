# Repository Guidelines

## Project Structure & Module Organization

This repository is currently a small starting point with Git metadata and a root ignore file named `.gitingore`. Keep new project files organized from the beginning:

- Place application source in `src/`.
- Place tests in `tests/` or beside source files using a clear suffix such as `.test.js`, `.spec.ts`, or `_test.py`, depending on the language adopted.
- Place static assets in `assets/` or framework-specific public directories such as `public/`.
- Keep generated output out of version control; existing ignore rules already cover common folders such as `dist/`, `build/`, `coverage/`, and `node_modules/`.

## Build, Test, and Development Commands

No build system or package manifest is present yet. Until one is added, use Git checks as the baseline:

- `git status --short` shows pending changes.
- `git diff` reviews unstaged edits before committing.
- `git log --oneline -5` checks recent commit style.

When a runtime is introduced, document the exact commands here and in `README.md`, for example `npm install`, `npm test`, `npm run dev`, or `make test`.

## Coding Style & Naming Conventions

Follow the conventions of the language and framework selected for the project. Prefer small modules with descriptive names, for example `src/user-profile/` or `src/apiClient.ts`. Use consistent indentation within each language: two spaces for JavaScript/TypeScript, four spaces for Python, and formatter defaults when a tool such as Prettier, ESLint, Black, or Ruff is added. Commit formatter and linter configuration with the code that depends on it.

## Testing Guidelines

Add tests alongside new behavior. Name tests after the unit or workflow being verified, such as `apiClient.test.ts` or `test_api_client.py`. Keep tests deterministic and avoid relying on local secrets, external accounts, or machine-specific paths. If coverage tooling is added, keep generated reports under `coverage/`, which is already ignored.

## Commit & Pull Request Guidelines

The current history contains one initial commit, `Init...`, so there is no established convention yet. Use short, imperative commit subjects going forward, for example `Add project guide` or `Implement user profile form`. Pull requests should include a concise description, validation steps or test output, linked issues when applicable, and screenshots for UI changes.

## Security & Configuration Tips

Do not commit secrets. The ignore rules exclude `.env` and `.env.*` while allowing `.env.example`; use that file to document required configuration keys without real values.
