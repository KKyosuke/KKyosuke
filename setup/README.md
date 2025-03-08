# Setup
A memorandum for building local mac environment

## Mac

## Applications

* [Chrome](https://www.google.com/intl/ja_jp/chrome/dr/download/?brand=FKPE&ds_kid=43700081544017055&gad_source=1&gclid=Cj0KCQiA8q--BhDiARIsAP9tKI080kkRiINW6rugyOhBi1tivuVgtfjMqfmtGNTv8Gzs1IEouf6_hfkaAn3UEALw_wcB&gclsrc=aw.ds)
* [Slack](https://slack.com/intl/ja-jp/)

## Homebrew
[Homebrew](https://brew.sh/)

### Install command
`brew install {package_name}`

### Packages
* [Neovim](https://neovim.io/)(=neovim)
* [colima](https://github.com/abiosoft/colima)(=colima)
    * Docker client is required for Docker runtime. Installable with brew `brew install docker`.
    * run `sudo ln -sf ~/.colima/docker.sock /var/run/docker.sock` to use in vs code

## Others
* [GO](https://go.dev/)
* [Rust](https://www.rust-lang.org/learn/get-started)
    * rustup: the Rust installer and version management tool
    * Cargo: the Rust build tool and package manager
* [nvm](https://github.com/nvm-sh/nvm)
    * directory変更時に.nvmrcの読み込み
        * [zshでの対応](https://github.com/nvm-sh/nvm?tab=readme-ov-file#zsh)
