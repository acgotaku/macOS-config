# macOS-config


## Screenshots

- 修改截图文件名前缀

  ```bash
  defaults write com.apple.screencapture name "screenshot"
  ```

- 修改截图文件保存路径

  ```bash
  mkdir -p ~/Documents/screenshots
  defaults write com.apple.screencapture location ~/Documents/screenshots
  ```


## Xcode

- 安装 Xcode (可选)

  - 通过 AppStore 安装(推荐) [Xcode](https://apps.apple.com/us/app/xcode/id497799835)

- 安装 Xcode Command Line Tools

  ```bash
  xcode-select --install
  ```

- 查看 Xcode Command Line Tools 路径

  ```bash
  xcode-select -p
  ```

## oh-my-zsh

- 安装 oh-my-zsh [官方网站](https://ohmyz.sh/#install)

  ```bash
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

- 配置环境变量

  ```bash
  echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/opt/homebrew/bin/brew shellenv)"
  ```


- 安装常用的软件

  ```bash
  brew install n git openssh zsh
  ```

- 安装常用的 cask

  ```bash
  brew install appcleaner google-chrome iina iterm2 keka kekaexternalhelper firefox microsoft-edge visual-studio-code vmware-fusion brave-browser
  ```

- 清理 Homebrew 缓存

  ```bash
  brew cleanup
  brew cleanup -s --prune=all
  ```
