<!-- !!! note 摘要
本文主要介绍在 Mac OS X 上安装 Nodejs 的方法参考以下链接
Homebrew 官方 https://brew.sh
NVM Github https://github.com/nvm-sh/nvm
!!! -->

## 安装 Hombrew

> [Homebrew](https://brew.sh)是 Mac OS X 上的软件包管理器，可以方便地从源代码编译安装软件包。它拥有安装、卸载、更新、查看、搜索等很多实用的功能，可以说是 Mac OS X 下最好用的开源软件包管理系统了。

### 官方脚本安装

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

执行完会提示要运行一行命令，如下
![](https://wxxb.cc/static/img/1697374606944.png)

复制粘贴到终端执行

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/xxx/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

### 配置生效

```bash
source ~/.zprofile
```

### 验证安装

```bash
# 查看版本
brew -v
# 查看安装路径
brew --repo
```

## 安装 NVM

### brew 安装

```bash
brew install nvm
```

### 根据提示配置环境变量

```bash

==> Caveats
Please note that upstream has asked us to make explicit managing
nvm via Homebrew is unsupported by them and you should check any
problems against the standard nvm install method prior to reporting.

You should create NVM's working directory if it doesn't exist:

mkdir ~/.nvm

Add the following to ~/.zshrc or your desired shell
configuration file:

export NVM_DIR="$HOME/.nvm"
[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
[ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion

You can set $NVM_DIR to any location, but leaving it unchanged from
/opt/homebrew/opt/nvm will destroy any nvm-installed Node installations
upon upgrade/reinstall.

Type `nvm help` for further information.
```

创建目录

```bash
mkdir ~/.nvm
```

配置环境环境变量

```bash

echo 'export NVM_DIR="$HOME/.nvm"
  [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion' >> ~/.zshrc
```

配置生效

```bash
source ~/.zshrc
```

## NVM 安装 Nodejs
