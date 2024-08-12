The Data Cleaning Workshop project welcomes contributions in a variety of forms.
This document contains information a few of the ways you can contribute to the Data Cleaning Workshop project.
Please also review our [Governance model](https://github.com/datarootsio/data-cleaning-workshop/blob/master/GOVERNANCE.md)

## Provide peer user support

We welcome users to the [Data Cleaning Workshop forum](https://github.com/datarootsio/data-cleaning-workshop) to ask questions and request assistance.
If you can help answer questions in your area of expertise, it would be a benefit to the community.

If a forum discussion determines there is a bug in Data Cleaning Workshop or a new feature is identified,
we welcome bug reports and feature requests. Please search the [issue tracker](https://github.com/datarootsio/data-cleaning-workshop) first to make sure
the bug / feature hasn't already been added. Note: the development team principally works from the issue
tracker, so anything not included there risks getting lost.

## Promote Data Cleaning Workshop

Promoting Data Cleaning Workshop is a great way to give back. Did you write a tutorial or article about Data Cleaning Workshop on your blog or site?
Are you organizing a workshop or presentation for Data Cleaning Workshop in your city? Let us, and the community, know via our [forum](https://github.com/datarootsio/data-cleaning-workshop) or social media.

## Contribute translations

We want Data Cleaning Workshop to be available in as many languages as possible to serve
the biggest community of users. You can help us [translate OpenRefine](https://github.com/datarootsio/data-cleaning-workshop) into languages you are fluent in [via Weblate](https://github.com/datarootsio/data-cleaning-workshop).
Although we have the beginnings of translations for many languages, only a few are complete and popular languages
like Spanish, Brazilian Portuguese, and French could use help.

## Contribute documentation

When browsing our [user manual](https://github.com/datarootsio/data-cleaning-workshop) or other documentation, feel free to use the edit button to suggest improvements.
For large changes, you might want to first discuss your proposed changes on the forum and then [prepare your changes locally](https://github.com/datarootsio/data-cleaning-workshop).

##  Contribute code 

You can contribute code in various ways:
- Fix bugs or implement new features. Follow [our guide towards your first code contribution](https://github.com/datarootsio/data-cleaning-workshop)
- Improve test coverage. Much of our code was originally written without tests, so help on this front is very much appreciated.
- Develop an Data Cleaning Workshop extension
- Develop a reconciliation service

All developers including new distributions and plugin developers are invited to leverage the following Data Cleaning Workshop project management areas.
- the [official documentation](https://github.com/datarootsio/data-cleaning-workshop) for shared documentation between both user docs and [technical reference](https://github.com/datarootsio/data-cleaning-workshop)
- the [developer forum](https://github.com/datarootsio/data-cleaning-workshop) for technical questions, new feature development and anything code related. We invite you to share your idea there first. Someone may be able to point out to existing development saving you hours of research and development.
- the [issue tracker](https://github.com/datarootsio/data-cleaning-workshop) for requesting new features and bug reports.
- [Gitter Chat](https://github.com/datarootsio/data-cleaning-workshop) (only occasionally monitored)

### How to submit PR's (pull requests), patches, and bug fixes

All code changes are made via GitHub Pull Requests which are reviewed before merging, even those by core committers.

If you are unfamiliar with git, GitHub, or open source development, please see [our guide towards your first code contribution](https://github.com/datarootsio/data-cleaning-workshop).

- If you are looking for something to work on, please see our [issue list](https://github.com/datarootsio/data-cleaning-workshop). We have a separate tag for [Good First Issues](https://github.com/datarootsio/data-cleaning-workshop).

- create a branch named with the issue number and a brief description
- avoid changes unrelated to fixing the issue
- create unit and/or end-to-end tests which cover the bug fix or new feature
- run `./refine lint` before submitting your PR (CI will fail if lint fails)
- make sure all tests are green before submitting your PR
- we attempt to prioritize PR reviews, but please be patient

### New functionality via extensions

Data Cleaning Workshop supports a plugin architecture to extend its functionality. You can find more information on how to write
an extension on our [website](https://github.com/datarootsio/data-cleaning-workshop).
Giuliano Tortoreto also wrote separate documentation detailing how to build an extension for Data Cleaning Workshop.
[PDF](https://github.com/datarootsio/data-cleaning-workshop) and [LaTeX](https://github.com/datarootsio/data-cleaning-workshop) versions are available. It dates from 2014, but still contains good information.

If you want your extension included in the [list of extensions](https://github.com/datarootsio/data-cleaning-workshop) advertised on openrefine.org,
please submit a pull request on the download page, please edit [this file](https://github.com/datarootsio/data-cleaning-workshop).
