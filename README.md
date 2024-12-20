# apt-install

[![CI](https://github.com/gerlero/apt-install/actions/workflows/ci.yml/badge.svg)](https://github.com/gerlero/apt-install/actions/workflows/ci.yml)
[![Release](https://github.com/gerlero/apt-install/actions/workflows/update-tags.yml/badge.svg)](https://github.com/gerlero/apt-install/actions/workflows/update-tags.yml)

GitHub Action to install and cache APT packages.

## Usage

```yaml
- uses: gerlero/apt-install@v1
  with:
    packages: curl
```

## Inputs

### `packages`

**Required**. A package name or a whitespace-separated list of package names to install.

### `cache` 

Whether to cache installed packages between runs. Default: `true`.

### `install-recommends`

Whether to install optional packages recommended by the packages to install. Default: `true`.

### `install-suggests`

Whether to install optional packages suggested by the packages to install. Default: `false`.

### `update`

Whether to update the package list (i.e., run `apt-get update`) before installing the packages. Default: `true`.

### `upgrade`

Whether to upgrade the listed packages if they are already installed and newer versions are available. Default: `true`.

## Related actions

- [`gerlero/add-apt-repository`](https://github.com/gerlero/add-apt-repository): GitHub Action to add a new APT repository for installing packages.
- [`gerlero/brew-install`](https://github.com/gerlero/brew-install): GitHub Action to install and cache Homebrew packages.
