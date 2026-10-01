# Contributing to the workshop

Read [EXERCISE.md](EXERCISE.md) and complete [the setup](README.md#setup) before starting.
Ask the facilitator about ambiguous reports or requirements. Record useful clarifications with your work.

## Working on a task

Create your own branch, for example `1-investigate-behavior`. Keep fixes for the first ticket ahead of feature work.
Use small commits that explain the change. Do not force-push or rewrite shared history.

Capture a reproducible observation before editing code. Compare competing explanations against evidence, then add a test
that fails for the behavior you intend to correct. For a feature, agree the expected behavior before implementing it.
Keep unrelated refactoring out of the change.

## Validation

Run these commands from the repository root after code changes:

```bash
./refine lint
./refine build
```

Then run tests appropriate to the affected code. `./refine test` runs the Java test suite;
`./refine server_test` and `./refine extensions_test` cover their respective areas.
Java tests live in module `src/test` directories and in `main/tests/server` and extension test directories.
New features should include unit and end-to-end tests for relevant behavior.

For frontend behavior, follow the [Cypress setup and test instructions](main/tests/cypress/Readme.md).
Inspect your diff after formatting and avoid submitting unrelated changes.

## Sharing results

Use the workshop repository for any issue discussion or pull request requested by your facilitator.
Describe the original behavior, the diagnosis supported by your evidence, and the result after the change.
Include relevant screenshots for UI changes, the test commands and results, and any limitations or unresolved questions.

Different implementations are welcome when they satisfy the agreed behavior and have convincing tests.
Follow the [Code of Conduct](CODE_OF_CONDUCT.md) and preserve existing copyright, license, and attribution notices.
