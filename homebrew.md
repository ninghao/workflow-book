# Homebrew

Homebrew 是用在 macOS 上的系统包管理工具。

[https://brew.sh/](https://brew.sh/)

## 安装

打开系统自带的终端工具，然后执行：

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

**brew**

安装成功以后，就可以使用 `brew` 命令去管理在 macOS 平台上的系统软件包了。

```
brew --help
```

## 使用

可以使用 Homebrew 安装的东西叫 formula ，其实就是一些软件，特别是一些命令行工具，开源软件，你可能都可以使用 Homebrew 安装。

遇到要安装的东西，先用 Homebrew 去搜索一下：

```
brew search 关键词
```

也可以在线搜索：

[http://braumeister.org/](http://braumeister.org/)

确定可以使用 Homebrew 安装，可以执行命令：

```
brew install 包的名字
```

删除使用 Homebrew 安装的软件，用的是：

```
brew uninstall 包的名字
```

## 练习

打开 macOS 系统上的终端，然后先试着用一下 wget 这个命令行工具：

```
→ wget
-bash: wget: command not found
```

会返回 command not found，系统上没这玩意。wget 可以在命令行界面下去下载网上的东西。

现在我们打算用 Homebrew 去安装一下在系统上不存在的 wget ，先搜索一下看看能不能用 Homebrew 安装它：

```
brew search wget
```

搜索到了两个结果：

```
wget wgetpaste
```

再确实一下找到的 wget 就是我想要用的东西：

```
brew info wget
```

会返回找到的这个 wget 相关的信息，根据提示应该可以判断这个就是我需要的东西，安装一下它，执行：

```
brew install wget
```

安装成功以后，再确定一下是否正确地安装了 wget，执行：

```
wget --help
```

这次就会返回一些帮助信息，说明 wget 已经可以用了。

