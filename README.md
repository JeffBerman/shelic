# SHELIC

SHELIC installs RELIC packages from a shell.  SHELIC is very simple and doesn't download packages like RELIC does; it merely works its way through the package's `build.txt` file and issues the same commands that RELIC would to compile and install the package.

Note: Not all RELIC commands are currently supported.  Simple projects seem to build fine.

## Usage

From a shell prompt:
```shell
$ cd some/package/directory
$ /path/to/shelic library_name
```

From a 5250 command line:
```shell
===> qsh
$ cd some/package/directory
$ /path/to/shelic library_name
```

## Installation

Just copy file `shelic` to a location in the IFS on your IBM i, and make sure it has execute privileges (it likely will).

## Why do I want this?

You probably don't, unless you're an IBM i software developer with very specific needs, or a tinkerer who doesn't want to install RELIC for some reason.

I wrote SHELIC because I'm releasing software that includes some third-party code as a submodule to my own project.  The third-party code uses RELIC to install, and I didn't want to require my users to install RELIC just to use my stuff.