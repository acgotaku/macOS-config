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

## Homebrew

- 安装 Homebrew [官方网站](https://brew.sh/zh-cn/)

  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
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
  brew install appcleaner google-chrome iina iterm2 keka kekaexternalhelper firefox microsoft-edge visual-studio-code vmware-fusion brave-browser squirrel
  ```

- 清理 Homebrew 缓存

  ```bash
  brew cleanup
  brew cleanup -s --prune=all
  ```

## iTerm2

- 配置关闭所有窗口时退出 iTerm2

  iTerm2 -> Settings -> General -> Closing, 选中 Quit when all windows are closed

- 禁用鼠标点击选中命令

  iTerm2 -> Settings -> General -> Selection, 取消选中 Click on a command selects it to restrict Find and Filter

- 修改主题颜色为黑色

  iTerm2 -> Settings -> Profiles -> Colors, 取消选中 Use different colors for light mode and dark mode, Color Presets 选择 Dark Background

## Rime for macOS

配置 squirrel 输入法， 参考 repo:

- [雾凇拼音](https://github.com/iDvel/rime-ice)
- [Rime configuration for Squirrel](https://github.com/alswl/Rime)

## 配置 Node 环境

我们使用 [n](https://github.com/tj/n) 来管理 Node 版本

- 配置环境变量到 .zshrc

  ```bash
  export N_PREFIX=$HOME/.n
  export PATH=$N_PREFIX/bin:$PATH
  ```

## GitHub

- 配置 GitHub 账号

  ```bash
  git config --global user.name "your_name"
  git config --global user.email "your_email@example.com"
  ```

## Office

- 禁用 office 自动更新

  ```bash
  launchctl unload -w /Library/LaunchAgents/com.microsoft.update.agent.plist
  ```
