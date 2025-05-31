# Setup
A memorandum for building local mac environment

## Mac

## Applications

* [Chrome](https://www.google.com/intl/ja_jp/chrome/dr/download/?brand=FKPE&ds_kid=43700081544017055&gad_source=1&gclid=Cj0KCQiA8q--BhDiARIsAP9tKI080kkRiINW6rugyOhBi1tivuVgtfjMqfmtGNTv8Gzs1IEouf6_hfkaAn3UEALw_wcB&gclsrc=aw.ds)
* [Slack](https://slack.com/intl/ja-jp/)

## [Homebrew](https://brew.sh/)

### Install command
`brew install {package_name}`  

### Packages
* [Lazygit](https://github.com/kdheepak/lazygit.nvim)(=lazygit)
    * set up [config](https://github.com/jesseduffield/lazygit/blob/master/docs/Config.md)
* [Hack](https://www.programmingfonts.org/#hack) (=font-Hack-nerd-font)
    * Needs to be set in Terminal Settings
* [Neovim](https://neovim.io/) (=neovim)
* [colima](https://github.com/abiosoft/colima) (=colima)
    * Docker client is required for Docker runtime. Installable with brew `brew install docker`.
    * run `sudo ln -sf ~/.colima/docker.sock /var/run/docker.sock` to use in vs code
    * run `ln -sfn $(which docker-buildx) ~/.docker/cli-plugins` to use buildx
    * to use docker compose
        * `brew install docker-compose`
        * `mkdir -p ~/.docker/cli-plugins`
        * `DOCKER_COMPOSE_PATH="$(which docker-compose)"`
        * `ln -sfn $DOCKER_COMPOSE_PATH ~/.docker/cli-plugins/docker-compose`

> [!NOTE]
> Manage background services using [Homebrew Services](https://github.com/Homebrew/homebrew-services?tab=readme-ov-file#homebrew-services)

## Others
* [GO](https://go.dev/)
* [Rust](https://www.rust-lang.org/learn/get-started)
    * rustup: the Rust installer and version management tool
    * Cargo: the Rust build tool and package manager
* [nvm](https://github.com/nvm-sh/nvm)
    * directory変更時に.nvmrcの読み込み
        * [zshでの対応](https://github.com/nvm-sh/nvm?tab=readme-ov-file#zsh)
