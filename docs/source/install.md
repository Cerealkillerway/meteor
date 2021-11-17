---
title: Install
---
Meteor currently supports **OS X, Windows, and Linux**. Only 64-bit is supported.
Apple M1 is only supported from Meteor 2.5.1 onward.

<h2 id="prereqs">Prerequisites and useful information</h2>

- Meteor requires Node.js 8 or newer installed for running the npm installer.
- Meteor supports Windows 7/Windows Server 2008 R2 and up.
- Disabling antivirus (Windows Defender, etc.) will improve performance.
- For compatibility, Linux binaries are built with CentOS 6.4 i386/amd64.
- iOS development requires the latest Xcode.
- **Do not install meteor npm in your project's package.json by any means, the npm library is only an installer.**

<h2 id="installation">Installation</h2>

Install the latest official Meteor release from your terminal:

```bash
npm install -g meteor
```

If your user doesn't have permission to install global binaries, and you need to use sudo, it's necessary to append *--unsafe-perm* to the above command:

```bash
sudo npm install -g meteor --unsafe-perm
```

We strongly discourage the usage of Node.js or Meteor with root permissions.
Only run the above command with sudo if you know what you are doing.

If you only use sudo because of a distribution default permission system, [check this link for fixing it](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally).

For Apple M1 computers, you can append Rosetta prefix as following:

```bash

arch -x86_64 npm install -g meteor

```

or select Terminal in the Applications folder, press CMD(⌘)+I and check the "Open using Rosetta" option.

We currently don't support Apple M1 native binaries as the latest meteor release uses Node.js 14 which doesn't have support for it until now. More info in our repository, [here](https://github.com/meteor/meteor/issues/11249#issuecomment-734327204).


<h2 id="legacy-install">Legacy Installation Method</h2>

For Linux and OS X, we are still providing the legacy installation method which uses a bash script and doesn't depend on Node.

```bash
curl https://install.meteor.com/ | sh
```

This installation method is not maintained anymore, and you should always use the NPM one.

<h2 id="meteor-docker">Run Meteor inside Docker</h2>

You can also use a Docker container for running Meteor inside your CI, or even in your local development toolchain.

We do provide the meteor/meteor-base ubuntu-based Docker image, that comes pre-bundled with Node.JS and Meteor, and runs it as a local user (not as root).

You can refer to our meteor/galaxy-images repository to see how to use it, and the latest version. [More about meteor-base here.](https://github.com/meteor/galaxy-images/blob/master/meteor-base/README.md)

<h2 id="fish-shell">Note for fish shell users (Linux)</h2>

To be able to user `meteor` command from fish it's needed to include `/home/<user>/.meteor` in `$PATH`; to do that just add this line in `/home/<user>/.config/fish/config.fish` file (replace `<user>` with your username):

`set PATH /home/<user>/.meteor $PATH`


