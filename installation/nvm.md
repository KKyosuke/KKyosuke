## About

[github](https://github.com/nvm-sh/nvm)

### Prerequisites

#### Installlation
location: `~/.nvm`

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

restart terminal / run `source ~/.zshrc` to load settings

### Commands

#### To download, compile, and install the latest release of node

```sh
nvm install node # "node" is an alias for the latest version
```

To install a specific version of node:

```sh
nvm install 14.7.0 # or 16.3.0, 12.22.1, etc
```

#### To set an alias

```sh
nvm alias my_alias v14.4.0
```
Make sure that your alias does not contain any spaces or slashes.

The first version installed becomes the default. New shells will start with the default version of node (e.g., `nvm alias default`).

#### Get currently active version

```
nvm current
```

#### Fix version for directory

```
node -v > .nvmrc
```

#### Auto switching

[zsh](https://github.com/nvm-sh/nvm?tab=readme-ov-file#zsh)

