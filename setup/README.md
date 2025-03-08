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
    * run `sudo ln -sf ~/.colima/docker.sock /var/run/docker.sock` to use in vs code

## Others
* [GO](https://go.dev/)
* [Rust](https://www.rust-lang.org/learn/get-started)
    * rustup: the Rust installer and version management tool
    * Cargo: the Rust build tool and package manager
* [nvm](https://github.com/nvm-sh/nvm)
    * `.zshrc`に以下を追加する
      ```
      # place this after nvm initialization!
      autoload -U add-zsh-hook
      load-nvmrc() {
        local node_version="$(nvm version)"
        local nvmrc_path="$(nvm_find_nvmrc)"

        if [ -n "$nvmrc_path" ]; then
          local nvmrc_node_version=$(nvm version "$(cat "${nvmrc_path}")")
      
          if [ "$nvmrc_node_version" = "N/A" ]; then
            nvm install
          elif [ "$nvmrc_node_version" != "$node_version" ]; then
            nvm use
          fi
        elif [ "$node_version" != "$(nvm version default)" ]; then
          echo "Reverting to nvm default version"
          nvm use default
        fi
      }
      add-zsh-hook chpwd load-nvmrc
      load-nvmrc
      ``` 
