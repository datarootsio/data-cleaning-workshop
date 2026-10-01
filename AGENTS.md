# Data Cleaning Workshop — agent guidance

This repository is a standalone dataroots workshop based on an existing Java application.
Read `EXERCISE.md` and the assigned workshop issue before changing behavior. Ask for missing requirements and distinguish
observations from hypotheses. Keep changes focused on the current task and retain existing authorship and license notices.

## Repository map

- `modules/core`: data model, operations, filtering, and project state.
- `modules/grel`: expression language.
- `main`: application integration, browser UI, and Cypress tests.
- `server`: embedded server and launcher support.
- `extensions`: database, Jython, PC-Axis, and Wikibase extensions.
- `packaging`: distribution assembly.
- `benchmark`: performance benchmarks.

The backend uses Java and a multi-module Maven build. The frontend uses JavaScript, jQuery, jQuery UI, Select2,
Underscore, and `@wikimedia/jquery.i18n`. Java tests use TestNG; browser tests use Cypress.

## Environment and commands

Use JDK 21–26, Apache Maven, Node.js 24+, and npm 11.16.0+.
Treat the root `pom.xml` and package manifests as the source of truth for dependency versions.

```bash
./refine build             # Build after code changes, before running or testing
./refine                   # Start the application at http://127.0.0.1:3333
./refine test              # Run the Java test suite
./refine server_test       # Run application/server tests
./refine extensions_test   # Run extension tests
./refine lint              # Apply repository source formatting
./refine e2e_tests         # Run browser tests; requires separate test dependency setup
```

See `main/tests/cypress/Readme.md` for browser-test setup and selecting a spec.
The E2E launcher starts its own server, so stop a running development server first.

Runtime options include `-d <data-directory>`, `-p <port>`, `-m <memory>`, `-i <interface>`, and `-c <config-path>`.
Use a separate workshop data directory for manual experiments.

## Change and review expectations

1. Work on your own issue branch; do not force-push or rewrite shared history.
2. Reproduce the report and collect evidence before proposing a cause.
3. Add tests that demonstrate the behavior being fixed or added. New features need unit and browser coverage where applicable.
4. Run `./refine lint` and `./refine build`, then the relevant tests. Inspect formatting changes for unrelated edits.
5. Report the exact checks run, their results, and any checks you could not run. Do not claim unexecuted tests passed.
6. Explain user-visible behavior and tradeoffs in the review description.

Follow `.editorconfig` and existing conventions. Keep translated UI strings in the appropriate `langs` files.
Keep extension-specific dependencies within their extension modules. Use the workshop repository for issues and reviews.
