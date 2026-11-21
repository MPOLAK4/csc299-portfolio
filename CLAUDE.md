# CSC299 portfolio: shared instructions

These rules apply to every project in this portfolio: `web-app-demo`,
`webapp-game`, and `headless-cmd-app`. Each project is its own git repo;
this repo only holds the README that links to them.

## Always write unit tests

- Whenever you create or change application code, write unit tests for it in the
  same step. Do not hand over an app without tests.
- Keep all tests in a top-level `tests/` folder, separate from the app code, so
  they are easy to leave out of a release.
- Use the standard test tool for the language (for Python, `pytest`). Run the
  tests before saying a change is done, and show me the result.
- Explain what each test checks and why, so I can learn to write them myself.

## Tests are for development, not for releases

- Tests stay in git (never put `tests/` in `.gitignore`), but they must not be
  shipped in a release version of the program.
- Keep them out of release builds/packages, for example with
  `tests/ export-ignore` in `.gitattributes` (affects `git archive`) or by
  excluding `tests/` in the packaging config.
- Release code must not import from `tests/` or depend on test-only packages.

## General

- Follow the root `CLAUDE.md` for how to teach, explain, and commit.
- Keep each project small and readable; I should be able to understand all of it.
