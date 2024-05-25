# aurci2

This repository uses the github action
[`kopp/build-aur-packages`](https://github.com/kopp/build-aur-packages)
to build
[AUR packages](https://aur.archlinux.org/)
and provide the built packages as
[release](https://github.com/z370q/aurci2/releases/tag/aurci2).

Build status:
![build status](https://github.com/z370q/aurci2/actions/workflows/build_repository.yaml/badge.svg?branch=master)


# Use this Repository with `pacman`

You can use these packages by adding the following to your `/etc/pacman.conf`:

```
[aurci2]
SigLevel = Optional TrustAll
Server = https://github.com/z370q/aurci2/releases/download/aurci2
```


# Build your own packages

Should you want to setup a similar repository for you, you can easily do so.

1. Fork this repository.
1. Modify the packages to be built in the file
   [`.github/workflows/build_repository.yaml`](.github/workflows/build_repository.yaml)
   (symlinked for convenience to [`build_repository.yaml`](build_repository.yaml)).
1. In the Actions tab, enable the actions.
