# Shelic

Shelic installs [Relic](https://github.com/OSSILE/RelicPackageManager) packages from a shell.  Shelic is very simple and doesn't download packages like Relic does; it merely works its way through an already-downloaded package's `build.txt` file and issues the same commands that Relic would to compile and install the package.

Note: Not all Relic commands are currently supported.  Simple projects seem to build fine.

## Installation

Just copy file `shelic` to a location in the IFS on your IBM i, and make sure it has execute privileges (it likely will).

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

or

```shell
===> qsh cmd('cd some/package/directory && /path/to/shelic library_name')
```

## Why do I want this?

You probably don't, unless you're an IBM i software developer with very specific needs, or a tinkerer who doesn't want to install Relic for some reason.

I wrote Shelic because I'm releasing software that includes some third-party code as a submodule to my own project.  The third-party code uses Relic to install, and I didn't want to require my users to install Relic just to use my stuff.