# 版本控制

你要为项目做版本控制，学会为项目做版本控制，是开发者的必备技能。用的工具叫 git。

## git

git 是一种版本控制工具，工具的使用只是一个熟练过程。

[https://git-scm.com/](https://git-scm.com/)

### 安装

可以在 git 官网下载适合自己操作系统上用的 git 。也可以使用系统包管理去安装 git，Windows 如果下载了完整版的 cmder ，里面已经包含了 git 。

**Windows**

Windows 系统，我推荐下载完整版的 cmder，它里面本身就包含了 git ，不再需要单独去安装了。

**macOS**

使用 Homebrew 安装 git：

```
brew install git
```

### 配置

告诉 git 你是谁，你的邮件地址是什么，这个邮件地址也应该是你在一些 git 服务商（比如：github，coding.net）那里注册帐号用的。

```
git config --global user.name 'wanghao'
git config --global user.email 'wanghao@ninghao.net'
```

上面两条命令，是在全局范围（`--global`）配置一下 git，设置了 `user.name` 用户名，还有 `user.email`  用户的邮件地址。以后你用 git 对项目做的提交（commit）里面都会自动包含这些配置信息。

---

1. 视频：[安装配置使用 git](https://ninghao.net/video/4571?a=51729)



