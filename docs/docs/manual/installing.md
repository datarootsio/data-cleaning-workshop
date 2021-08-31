---
id: installing
title: Installing Data Cleaning Workshop
sidebar_label: Installing
---

## System requirements {#system-requirements}

Data Cleaning Workshop does not require internet access to run its basic functions. Once you download and install it, it runs as a small web server on your own computer, and you access that local web server by using your browser. It only requires an internet connection to import data from the web, reconcile data using a web service, or export data to the web.

Data Cleaning Workshop requires three things on your computer in order to function:

#### Compatible operating system {#compatible-operating-system}

Data Cleaning Workshop is designed to work with **Windows**, **Mac**, and **Linux** operating systems. [Our team releases packages for each](https://github.com/datarootsio/data-cleaning-workshop).

#### Java {#java}

[Java](https://java.com/en/download/) must be installed and configured on your computer to run Data Cleaning Workshop. The Mac version of Data Cleaning Workshop includes Java; new in Data Cleaning Workshop 3.4, there is also a Windows package with Java included.

If you install and start Data Cleaning Workshop on a Windows computer without Java, it will automatically open up a browser window to the [Java downloads page](https://java.com/en/download/), and you can simply follow the instructions there.

We recommend you [download](https://java.com/en/download/) and install Java before proceeding with the Data Cleaning Workshop installation. Please note that Data Cleaning Workshop works with Java 14 but not Java 16 or later versions, hopefully this will be fixed in the 3.5 final release (see issue [#4106](https://github.com/datarootsio/data-cleaning-workshop)).

#### Compatible browser {#compatible-browser}

OpenRefine works best on browsers based on Webkit, such as:

*   Google Chrome
*   Chromium
*   Opera
*   Microsoft Edge

We are aware of some minor rendering and performance issues on other browsers such as Firefox. We don't support Internet Explorer. If you are having issues running Data Cleaning Workshop, see the [section on Running](running.md#troubleshooting).

### Release versions {#release-versions}

Data Cleaning Workshop always has a [latest stable release](https://github.com/datarootsio/data-cleaning-workshop), as well as some more recent developments available in beta, release candidate, or [snapshot releases](https://github.com/datarootsio/data-cleaning-workshop). If you are installing for the first time, we recommend [the latest stable release](https://github.com/datarootsio/data-cleaning-workshop).

If you wish to use an extension that is only compatible with an earlier version of Data Cleaning Workshop, and do not require the latest features, you may find that [an older stable version is best for you](https://github.com/datarootsio/data-cleaning-workshop) in our list of releases. Look at later releases to see which security vulnerabilities are being fixed, in order to assess your own risk tolerance for using earlier versions. Look for “final release” versions instead of “beta” or “release candidate” versions.

#### Unstable versions {#unstable-versions}

If you need a recently developed function, and are willing to risk some untested code, you can look at [the most recent items in the list](https://github.com/datarootsio/data-cleaning-workshop) and see what changes appeal to you.

“Beta” and “release candidate” versions may both have unreported bugs and are most suitable for people who are willing to help us troubleshoot these versions by [creating bug reports](https://github.com/datarootsio/data-cleaning-workshop).  

For the absolute latest development updates, see the [snapshot releases](https://github.com/datarootsio/data-cleaning-workshop). These are created with every commit.

#### What’s changed {#whats-changed}

Our [latest version is Data Cleaning Workshop 3.4.1](https://github.com/datarootsio/data-cleaning-workshop), released September 24th 2020. The major changes in this version are listed on the [3.4.1 release page](https://github.com/datarootsio/data-cleaning-workshop) with the downloadable packages.

You can find information about all Data Cleaning Workshop versions on the [Releases page on Github](https://github.com/datarootsio/data-cleaning-workshop).

:::info Other distributions
Data Cleaning Workshop may also work in other environments, such as [Chromebooks](https://gist.github.com/organisciak/3e12e5138e44a2fed75240f4a4985b4f) where Linux terminals are available. Look at our list of [Other Distributions on the Downloads page](https://github.com/datarootsio/data-cleaning-workshop) for other ways of running Data Cleaning Workshop, and refer to our contributor community to see new environments in development.
:::

## Installing or upgrading {#installing-or-upgrading}
### Back up your data {#back-up-your-data}

If you are upgrading from an older version of Data Cleaning Workshop and have projects already on your computer, you should create backups of those projects before you install a new version.

First, [locate your workspace directory](#where-is-data-stored). Then copy everything you find there and paste it into a folder elsewhere on your computer.

For extra security you can [export your existing Data Cleaning Workshop projects](exporting#export-a-project).

:::caution
Take note of the [extensions](#installing-extensions) you have currently installed. They may not be compatible with the upgraded version of Data Cleaning Workshop. Installations can be installed in two places, so be sure to check both your workspace directory and the existing installation directory.
:::

### Install or upgrade Data Cleaning Workshop {#install-or-upgrade-openrefine}

If you are upgrading an existing Data Cleaning Workshop installation, you can delete the old program files and install the new files into the same space. Do not overwrite the files as some obsolete files may be left over unnecessarily.

:::caution
If you have extensions installed, do not delete the `webapp\extensions` folder where you installed them. You may wish to install extensions into the workspace directory instead of the program directory. There is no guarantee that extensions will be forward-compatible with new versions of Data Cleaning Workshop, and we do not maintain extensions.
:::

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs
  groupId="operating-systems"
  defaultValue="win"
  values={[
    {label: 'Windows', value: 'win'},
    {label: 'Mac', value: 'mac'},
    {label: 'Mac via Homebrew', value: 'mac-hb'},
    {label: 'Linux', value: 'linux'}
  ]
}>

<TabItem value="win">

Once you have downloaded the `.zip` file, extract it into a folder where you wish to store program files (such as `D:\Program Files\OpenRefine`).

You can right-click on `openrefine.exe` or `refine.bat` and pin one of those programs to your Start Menu or create shortcuts for easier access.

</TabItem>

<TabItem value="mac">

Once you have downloaded the `.dmg` file, open it and drag the Data Cleaning Workshop icon onto the Applications folder icon (just like you would normally install Mac applications).

</TabItem>

<TabItem value="mac-hb">

The quick version:

1. Install [Homebrew](http://brew.sh)
2. In Terminal enter ` brew cask install openrefine`
1. Then find Data Cleaning Workshop in your Applications folder.

The long version:

[Homebrew](http://brew.sh) is a popular command-line package manager for Mac. Installing Homebrew is accomplished by pasting the installation command on the Homebrew website into a Terminal window. Once Homebrew is installed, applications like Data Cleaning Workshop can be installed via a simple command. You can [install Homebrew from their website](http://brew.sh).

###### Install {#install}

Install Data Cleaning Workshop with this command:

```
brew cask install openrefine
```

You should see output like this:

```
==> Downloading https://github.com/OpenRefine/OpenRefine/releases/download/2.7/openrefine-mac-2.7.dmg
########################### 100.0%
  ==> Verifying checksum for Cask openrefine
  ==> Installing Cask openrefine
  ==> Moving App 'OpenRefine.app' to '/Applications/OpenRefine.app'.
  🍺  openrefine was successfully installed!
```

Behind the scenes, this command causes Homebrew to download the Data Cleaning Workshop installer, verify the file’s authenticity (using a SHA-256 checksum), mount the disk image, copy the `OpenRefine.app` application bundle into the Applications folder, unmount the disk image, and save a copy of the installer and metadata about the installation for future use.

If an existing `OpenRefine.app` is found in the Applications folder, Homebrew will not overwrite it, so installing via Homebrew requires either deleting or renaming previously installed copies.

###### Uninstall {#uninstall}

To uninstall Data Cleaning Workshop, paste this command into the Terminal:

```
 brew cask uninstall openrefine
```

You should see output like this:

```
 ==> Removing App '/Applications/OpenRefine.app'.
```

###### Update {#update}

To update to the latest version of Data Cleaning Workshop, paste this command into the Terminal:

```
 brew cask reinstall openrefine
```

You should see output like this:

```
 ==> Downloading https://github.com/OpenRefine/OpenRefine/releases/download/2.7/openrefine-mac-2.7.dmg
########################### 100.0%
  ==> Verifying checksum for Cask openrefine
  ==> Removing App '/Applications/OpenRefine.app'.
  ==> Moving App 'OpenRefine.app' to '/Applications/OpenRefine.app'.
  🍺  openrefine was successfully installed!
```

If you had previously installed the `openrefine-dev` cask (containing a release candidate) and you want to move to the stable release, you need to first uninstall the old cask and then install the new one:

```
 brew cask uninstall openrefine-dev
 brew cask install openrefine
```
</TabItem>

<TabItem value="linux">

Once you have downloaded the `.tar.gz` file, open a shell, navigate to the folder containing the download, and type:

```
tar xzf openrefine-linux-3.4.tar.gz
```

</TabItem>

</Tabs>

---


### Set where data is stored {#set-where-data-is-stored}

Data Cleaning Workshop stores data in two places: program files in the program directory, wherever it is you’ve installed it; and project files in what we call the “workspace directory.” You can access this folder easily from Data Cleaning Workshop by going to the [home screen](running#the-home-screen) (at [http://127.0.0.1:3333/](http://127.0.0.1:3333/)) and clicking <span class="buttonLabels">Browse workspace directory</span>.

By default this is:

<Tabs
  groupId="operating-systems"
  defaultValue="win"
  values={[
    {label: 'Windows', value: 'win'},
    {label: 'Mac', value: 'mac'},
    {label: 'Linux', value: 'linux'}
  ]
}>

<TabItem value="win">

Depending on your version of Windows, the data is in one of these directories:
*   `%appdata%\OpenRefine`
*   `%localappdata%\OpenRefine`
*   `C:\Documents and Settings\(user id)\Local Settings\Application Data\OpenRefine`
*   `C:\Users\(user id)\AppData\Roaming\OpenRefine`
*   `C:\Users\(user id)\AppData\Local\OpenRefine`
*   `C:\Users\(user id)\OpenRefine`

For older Data Cleaning Workshop releases, replace `OpenRefine` with `Google\Refine`.

You can change this by adding this line to the file `openrefine.l4j.ini` and specifying your desired drive and folder path:

```
-Drefine.data_dir=D:\MyDesiredFolder
```

If your folder path has spaces, use neutral quotation marks around it:

```
-Drefine.data_dir="D:\My Desired Folder"
```

If the folder does not exist, Data Cleaning Workshop will create it.

</TabItem>

<TabItem value="mac">

```
~/Library/Application Support/OpenRefine/
```

For older versions, as Data Cleaning Workshop:

```
~/Library/Application Support/Google/Refine/
```

Logging is to `/var/log/daemon.log` - grep for `com.google.refine.Refine`.

</TabItem>

<TabItem value="linux">

```
~/.local/share/openrefine/
```

You can change this when you run Data Cleaning Workshop from the terminal, by pointing to the workspace directory through the `-d` parameter:

```
 ./refine -p 3333 -i 0.0.0.0 -m 6000M -d /My/Desired/Folder
```

</TabItem>

</Tabs>

---


### Logs {#logs}

Data Cleaning Workshop does not currently output an error log, but because the Data Cleaning Workshop console window is always open (on Linux and Windows) while Data Cleaning Workshop runs in your browser, you can copy information from the console if an error occurs.

Using a Mac, you can [run Data Cleaning Workshop using the terminal](running#starting-and-exiting) in order to capture errors.

---

## Increasing memory allocation {#increasing-memory-allocation}

Data Cleaning Workshop relies on having computer memory available to it to work effectively. If you are planning to work with large datasets, you may wish to set up Data Cleaning Workshop to handle it at the outset. By “large” we generally mean one of the following indicators:
*   more than one million total cells
*   an input file size of more than 50 megabytes (MB)
*   more than 50 [rows per record in records mode](running#records-mode)

By default Data Cleaning Workshop is set to operate with 1 gigabyte (GB) of memory (1024MB). If you feel that Data Cleaning Workshop is running slowly, or you are getting “out of memory” errors (for example, `java.lang.OutOfMemoryError`), you can try allocating more memory.

A good practice is to start with no more than 50% of whatever memory is left over after the estimated usage of your operating system, to leave memory for your browser to run.

All of the settings below use a four-digit number to specify the megabytes (MB) used (actually [mebibytes](https://en.wikipedia.org/wiki/Mebibyte)). The default is usually 1024MB, but the new value doesn't need to be a multiple of 1024.

:::info Dealing with large datasets
If your project is big enough to need more than the default amount of memory, consider turning off <span class="fieldLabels">Parse cell text into numbers, dates, ...</span> on import. It's convenient, but less efficient than explicitly converting any columns that you need as a data type other than the default “string” type.
:::

<Tabs
  groupId="operating-systems"
  defaultValue="win"
  values={[
    {label: 'Windows', value: 'win'},
    {label: 'Mac', value: 'mac'},
    {label: 'Linux', value: 'linux'}
  ]
}>

<TabItem value="win">

#### Using openrefine.exe {#using-openrefineexe}

If you run `openrefine.exe`, you will need to edit the `openrefine.l4j.ini` file found in the program directory and edit the line

```
# max memory memory heap size
-Xmx1024M
```

The line “-Xmx1024M” defines the amount of memory available in megabytes. Change the number “1024” - for example, edit the line to “-Xmx2048M” to make 2048MB [2GB] of memory available.

:::caution openrefine.exe not running?
Once you increase the memory allocation, you may find that you cannot run `openrefine.exe`. In this case, your computer needs a 64-bit version of [Java](https://www.java.com/en/download/help/index_installing.xml) (this is different from [Java JDK](#install-or-upgrade-java). Look for the “Windows Offline (64-bit)” download on the Downloads page and install that. Your system must also be set to use the 64-bit version of Java by [changing the Java configuration](https://www.java.com/en/download/help/update_runtime_settings.xml).
:::

#### Using refine.bat {#using-refinebat}

On Windows, Data Cleaning Workshop can also be run by using the file `refine.bat` in the program directory. If you start Data Cleaning Workshop using `refine.bat`, the memory available to Data Cleaning Workshop can be specified either through command line options, or through the `refine.ini` file.

To set the maximum amount of memory on the command line when using `refine.bat`, `cd` to the program directory, then type

```refine.bat /m 2048m```

where “2048” is the maximum amount of MB that you want OpenRefine to use.

To change the default that `refine.bat` uses, edit the `refine.ini` line that reads

```REFINE_MEMORY=1024M```

Note that this file is only read if you use `refine.bat`, not `openrefine.exe`.

</TabItem>
<TabItem value="mac">

If you have downloaded the `.dmg` package and you start Data Cleaning Workshop by double-clicking on it:

*   close Data Cleaning Workshop
*   control-click on the Data Cleaning Workshop icon (opens the contextual menu)
*   click on "show package content” (a finder window opens)
*   open the “Contents” folder
*   open the `Info.plist` file with any text editor (like Mac's default TextEdit)
*   Change “-Xmx1024M” into, for example, “-Xmx2048M” or “-Xmx8G”
*   save the file
*   restart Data Cleaning Workshop.

</TabItem>
<TabItem value="linux">

If you have downloaded the `.tar.gz` package and you start Data Cleaning Workshop from the command line, add the “-m xxxxM” parameter like this:
`./refine -m 2048m`

#### Setting a default {#setting-a-default}

If you don't want to set this option on the command line each time, you can also set it in the `refine.ini` file. Edit the line

```
REFINE_MEMORY=1024M
```

Make sure it is not commented out (that is, that the line doesn't start with a “#” character), and change “1024” to a higher value. Save the file, and when you next start Data Cleaning Workshop it will use this value.

</TabItem>

</Tabs>

---


## Installing extensions {#installing-extensions}

Extensions have been created by our contributor community to add functionality or provide convenient shortcuts for common uses of OpenRefine. [We list extensions we know about on our downloads page](https://openrefine.org/download.html).

:::info Contributing extensions
If you’d like to create or modify an extension, [see our developer documentation here](https://github.com/datarootsio/data-cleaning-workshop). If you’re having a problem, [use our downloads page](https://github.com/datarootsio/data-cleaning-workshop) to go to the extension’s page and report the issue there.
:::

### Two ways to install extensions {#two-ways-to-install-extensions}

You can [install extensions in one of two places](#set-where-data-is-stored):

*   Into your Data Cleaning Workshop program folder, so they will only be available to that version/installation of Data Cleaning Workshop (meaning the extension will not run if you upgrade Data Cleaning Workshop), or
*   Into your workspace, where your projects are stored, so they will be available no matter which version of Data Cleaning Workshop you’re using.

We provide these options because you may wish to reinstall a given extension manually each time you upgrade Data Cleaning Workshop, in order to be sure it works properly.

### Find the right place to install {#find-the-right-place-to-install}

If you want to install the extension into the program folder, go to your program directory and then go to `webapp\extensions` (or create it if not does not exist).

If you want to install the extension into your workspace, you can:
*   launch Data Cleaning Workshop and click <span class="menuItems">Open Project</span> in the sidebar
*   At the bottom of the screen, click <span class="menuItems">Browse workspace directory</span>
*   A file-explorer or finder window will open in your workspace
*   Create a new folder called “extensions” inside the workspace if it does not exist.

You can also [find your workspace on each operating system using these instructions](#set-where-data-is-stored).  

### Install the extension {#install-the-extension}

Some extensions have their own instructions: make sure you read the documentation before you begin installing.

Some extensions may have multiple versions, to match Data Cleaning Workshop versions, so be sure to choose the right release for your installation. If you have questions about compatibility or want to request or voice your support for an update, [use our downloads page](https://github.com/datarootsio/data-cleaning-workshop) to go to the extension’s page and report the issue there.

Generally, the installation process will be:

*   Download the extension (usually as a zip file from GitHub)
*   Extract the zip contents into the “extensions” directory, making sure all the contents go into one folder with the name of the extension
*   Start (or restart) Data Cleaning Workshop.

To confirm that installation was a success, follow the instructions provided by the extension. Each extension will appear in its own way inside the Data Cleaning Workshop interface. Make sure you read its documentation to know where the functionality will appear, such as under specific dropdown menus.
