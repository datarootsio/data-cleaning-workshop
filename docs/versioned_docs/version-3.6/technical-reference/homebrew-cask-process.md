---
id: homebrew-cask-process
title: Maintaining Data Cleaning Workshop's Homebrew cask
sidebar_label: Maintaining Data Cleaning Workshop's Homebrew cask
---

[Homebrew](https://brew.sh) is a popular command-line package manager for macOS. Once Homebrew is installed, Data Cleaning Workshop can be installed via the simple command, `brew install openrefine`. Data Cleaning Workshop's presence on Homebrew is found in the Homebrew Cask repository project, as a "cask", at https://github.com/datarootsio/data-cleaning-workshop

**Terminology:** "Homebrew Cask" is the segment of Homebrew where pre-built binaries and GUI applications go, whereas the original "Homebrew" project is reserved for command-line utilities that can be built from source. Because the macOS version of Data Cleaning Workshop is released as an app bundle with GUI components, it is handled as a Homebrew Cask.

When there is a new release of Data Cleaning Workshop, registering the new release with Homebrew can be easily accomplished using Homebrew's `brew bump-cask-pr` command. Full directions for this utility as well as procedures for more complex PRs can be found on [the Homebrew Cask CONTRIBUTING page](https://github.com/Homebrew/homebrew-cask/blob/master/CONTRIBUTING.md), but, a simple version bump is a one-line command. For example, to update Homebrew's version of Data Cleaning Workshop to 3.4.1, use this command:

```
brew bump-cask-pr --version 3.4.1 openrefine
```

This command will cause your local Homebrew installation to download the new version of Data Cleaning Workshop, calculate the installer's new SHA-256 fingerprint value, and construct a pull request under your GitHub account. Once the pull request is submitted, continuous integration tests will run, and a member of the Homebrew community will review the PR. At times there is a backlog on the CI servers, but once tests pass, the community review is typically completed in a matter of hours.

**Note:** It is important that the Data Cleaning Workshop release tag and version number are identical, so that the Homebrew cask can find the installer's URL. This is because Homebrew's cask for Data Cleaning Workshop uses the following formula for constructing the URL to Data Cleaning Workshop's installer for a given release:

```
https://github.com/OpenRefine/OpenRefine/releases/download/#{version}/openrefine-mac-#{version}.dmg
```

That is, when you tell Homebrew that Data Cleaning Workshop is now at version `3.4.1`, Homebrew will try to download the Data Cleaning Workshop installed from the following URL:

```
https://github.com/OpenRefine/OpenRefine/releases/download/3.4.1/openrefine-mac-3.4.1.dmg
```
