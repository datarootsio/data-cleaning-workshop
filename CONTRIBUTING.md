This document present how you can contribute to the Data Cleaning Workshop project. Please review also our [Governance model](https://github.com/datarootsio/data-cleaning-workshop/blob/master/GOVERNANCE.md)

## Documentation, Questions or Problem

Our issue list is only for reporting specific bugs and requesting specific features. If you just don't know how to do something using Data Cleaning Workshop, or want to discuss some ideas, please
- try the [documentation wiki](https://github.com/datarootsio/data-cleaning-workshop)
- ask on the [Data Cleaning Workshop mailing list](https://github.com/datarootsio/data-cleaning-workshop).

If you really want to file a bug or request a feature, go to this [issue list](https://github.com/datarootsio/data-cleaning-workshop). Please use the search function first to make sure a similar issue doesn't already exist. 

### Guidelines for Reporting a Bug

When reporting a bug please provide the following information to help reproduce the bug:
- Version of Data Cleaning Workshop used (Data Cleaning Workshop 2.6, OpenRefine2.7, an other distribution?)
- Operating Systems and version
- Browser + version used - Please note that Data Cleaning Workshop doesn't support Internet Explorer
- Steps followed to create the issue
- If you are allowed, it is awesome if you can include the data generating the issue
- Current Results
- Expected Results


## Promote Data Cleaning Workshop

You don't need to be coder to contribute to Data Cleaning Workshop. Did you write a tutorial or article about Data Cleaning Workshop on your blog or site? Are you organizing a workshop or presentation for Data Cleaning Workshop in your city? Let us know via our [user discussion list](https://github.com/datarootsio/data-cleaning-workshop) or Twitter account ([@OpenRefine](https://github.com/datarootsio/data-cleaning-workshop)). We will share the news via our monthly update and via our Twitter handle. 

## Contributing translations

You can help us [translate OpenRefine](https://github.com/datarootsio/data-cleaning-workshop) in as many languages as possible [via Weblate](https://github.com/datarootsio/data-cleaning-workshop).

##  Contributing code 

You can contribute code in three different ways:
- fix minor bugs
- develop an Data Cleaning Workshop extension 
- start your own distribution or fork

All developers including new distributions and plugin developers are invited to leverage the following Data Cleaning Workshop project management areas to avoid the dispersion of the community in different communication channels.
- the [wiki](https://github.com/datarootsio/data-cleaning-workshop) for shared documentation between both user docs and [documentation for developer](https://github.com/datarootsio/data-cleaning-workshop)
- the [developer mailing list](https://github.com/datarootsio/data-cleaning-workshop) for technical questions, new feature development and anything code related. We invite you to share you idea first via the developer mailing list. Someone may be able to point out to existing development saving you hours of research and development. 
- [Data Cleaning Workshop github issue tracker](https://github.com/datarootsio/data-cleaning-workshop) for requesting new features and bug reports.

### How to submit PR's (pull requests), patches, and bug fixes

- Avoid merging master in your branch because it makes code review a lot harder.
- If you want to keep your branch up to date with our master, it would be nicer if you could just rebase your branch instead. That would keep the history a lot cleaner.
- Please avoid adding unrelated changes in the PR. Do a separate PR and rebase once they get merged can work really well.
 
If you make trivial changes, you can send them directly via a pull request. **Please make your changes in a new git branch and send your patch**, including appropriate test cases.

We want to keep the quality of the trunk at a very high level, since this is ultimately where the Stable Releases are built from after bugs are fixed. Please take the time to test your changes (including travis-ci) before sending a pull request.

Data Cleaning Workshop is volunteer supported. Pull Requests are reviewed and merged by volunteers. All Pull Requests will be answered, however it may take some time to get back to you. Thank you in advance for your patience.

If you don't know where to start and are looking for a bug to fix, please see our [issue list](https://github.com/datarootsio/data-cleaning-workshop). 

### New functionalities via extensions

Data Cleaning Workshop support a plugin architecture to extend its functionality. You can find more information on how to write extension on [our wiki](https://github.com/datarootsio/data-cleaning-workshop). Giuliano Tortoreto wrote a separate documentation detailling how to build extension for Data Cleaning Workshop. A [LaTeX](https://github.com/datarootsio/data-cleaning-workshop) and [PDF version](https://github.com/datarootsio/data-cleaning-workshop) are available.

If you want to list your extension on the download page, please edit [this file](https://github.com/datarootsio/data-cleaning-workshop).

### New distributions

Data Cleaning Workshop is already available in many different distributions (see the [download page](https://github.com/datarootsio/data-cleaning-workshop)). New distributions often package Data Cleaning Workshop for a specific usage or port it. We are fine with new forks ([see discussion](https://github.com/datarootsio/data-cleaning-workshop)) but we invite you to engage with the community to share your roadmap and progress.

Github offers a powerful system to work between different repositories and we encourage you to leverage it:
- You can cross reference issues and pull requests between Github repository using `user/repository#number` ([see more here](https://github.com/blog/967-github-secrets#cross-repository-issue-references))
- If you want to merge a Pull Request that is pending for review to your own repository check the pull request locally ([see more here](https://help.github.com/articles/checking-out-pull-requests-locally/)).

Don't forget to contribute to the upstream (main Data Cleaning Workshop) repository so your changes from your distribution can be reviewed and merged and to keep other developers aware of your progress. If you want to list your distribution on the download page, please edit [this file](https://github.com/datarootsio/data-cleaning-workshop).
