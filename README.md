# Data Cleaning Workshop

A hands-on workshop in diagnosing unfamiliar software, testing changes, and turning a user request into a useful feature.
The application lets you import tabular data, inspect it, and clean it in a local browser.

Start with [EXERCISE.md](EXERCISE.md) for the workshop tasks.

## Setup

Install JDK 21–26, Apache Maven, Node.js 24 or newer, and npm 11.16.0 or newer.
The Java version limits are defined in `pom.xml`; frontend requirements are in `main/webapp/package.json`.

```bash
git clone https://github.com/datarootsio/data-cleaning-workshop.git
cd data-cleaning-workshop
./refine build
./refine
```

Open http://127.0.0.1:3333. On Windows, use `refine.bat build` and `refine.bat`.
Stop the application with Ctrl+C in its terminal.

Use `./refine -d /path/to/workshop-data` to keep workshop projects in a separate data directory.
Use `./refine -p 3334` if the default port is occupied.

## Working in the repository

- [Exercise](EXERCISE.md): tasks and what to bring to the discussion.
- [Contributing](CONTRIBUTING.md): branches, validation, and review.
- [Agent guidance](AGENTS.md): repository layout and commands.
- [UI tests](main/tests/cypress/Readme.md): end-to-end test setup.

This repository is maintained for the dataroots workshop. Use its
[issue tracker](https://github.com/datarootsio/data-cleaning-workshop/issues) for workshop questions,
or ask your facilitator during the session.

## Credits and license

This workshop is derived from OpenRefine, created by Metaweb Technologies, Inc. and originally conceived and written
by David Huynh. It became Google Refine after Google's acquisition of Metaweb in 2010, then the community project
OpenRefine in 2012. The application includes work by its many contributors; existing authorship and copyright notices
are retained. This workshop is maintained independently of that project.

The code is distributed under the BSD-3-Clause license in [LICENSE.txt](LICENSE.txt).
Third-party notices remain in [packaging/THIRD-PARTY.txt](packaging/THIRD-PARTY.txt),
`main/webapp/licenses`, and the extension license directories.
