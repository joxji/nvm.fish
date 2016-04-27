[slack-link]: https://fisherman-wharf.herokuapp.com
[slack-badge]: https://fisherman-wharf.herokuapp.com/badge.svg
[travis-link]: https://travis-ci.org/fisherman/fisherman
[travis-badge]: https://img.shields.io/travis/fisherman/fisherman.svg

[![][travis-badge]][travis-link]
[![][slack-badge]][slack-link]

# fin

fin is a node version manager using ideas from [tj/n], [wbyoung/avn] and [creationix/nvm] for the fish shell.

## Features

* Autocomplete

* No configuration

* Cached downloads

* Automatic version switching

* No sudo, version is selected by prepending to `$PATH`

## Install

```
fisher fin
```

## Usage

Use node 5.5.0.

```
fin 5.5.0
node -v
v5.5.0
```

Use a *.finrc* file.

```
echo 5.10.1 > .finrc
node -v
v5.10.1
```

Use the latest stable node release.

```
fin latest
```

Use the latest LTS (long-term support) node release.

```
fin lts
```

Select a version interactively.

```
fin
  5.5.0
  5.10.0
* 5.10.1
```

List all versions available for download.

```
fin ls
  ...
- 5.5.0
  5.6.0
  ...
  5.9.1
- 5.10.0
* 5.10.1
```

> Version is currently selected: `*`
> Version is already downloaded: `-`

Remove a version.

```
fin rm 5.5.0
```

## Bugs

fin was built for fish >= 2.3.0. If you are using fish 2.2.0, append the following code to your ~/.config/fish/config.fish for automatic version switching support.

```fish
for file in ~/.config/fish/conf.d/*.fish
    source $file
end
```

[bass]: https://github.com/edc/bass
[laborious]: https://github.com/edc/bass/issues/28
[tj/n]: https://github.com/tj/n
[wbyoung/avn]: https://github.com/wbyoung/avn
[creationix/nvm]: https://github.com/creationix/fin
