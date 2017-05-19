# ssh-key

管理服务器，向 git 远程推送代码，做这些事之前都需要先验证你的身份，一般就是使用你的用户名与密码。ssh-key 可以让你不再输入用户名与密码就能做这些事。在你电脑上生成 ssh-key ，它是一对，一个私钥（Private key），一个公钥（Public key）。

然后你去配置一下服务（服务器，git 远程服务 ... ），把你生成的 ssh-key 的公钥告诉这些服务。这样你再使用这些服务的时候，就会根据你提供给服务的公钥，还有在你电脑上的私钥，如果匹配，就能通过身份的验证了。

## 生成

这个动作你只需要做一次，最好也只做一次，因为每次你生成的 ssh-key 都是不一样的，这样会影响到你之前使用了 ssh-key 的地方。

Windows 用户打开 cmder，新建一个 mintty 类型的标签。macOS 用户打开终端，先看一下之前有没有生成过 ssh-key，执行：

```
ls ~/.ssh
```

如果是空白，或者显示没有这个目录，那说明你之前没生成过 ssh-key，如果 .ssh 里面有两个文件，id\_rsa，还有 id\_rsa.pub ，说明你已经有了 ssh-key ，就不需要再次生成了它了，你可以直接使用 id\_rsa.pub 这个公钥去配置服务的验证了。

如果没有，生成 ssh-key，执行命令：

```
ssh-keygen
```

命令的返回的信息里会告诉你生成的 ssh-key 会放在哪里，一般就是用户主目录下的 .ssh 这个目录的下面。还会让你输入密码短语，可以不设置，直接接回车就行。

## 使用

你在配置服务使用 ssh-key 的方式登录的时候，只需要告诉服务你的 ssh-key 里的公钥文件里的内容就行了。查看公钥文件里的内容，执行：

```
cat ~/.ssh/id_rsa.pub
```

会返回类似的东西：

```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC3V80xP8acswtv8OMpsjWGk3BsHiajtAYk/4suPkwvIPgfz1+XNTRR8wNvmuExsT5ynTWX7evPlwNxGQqRiO7TKsN8g9/N9E0RhHwfrOh0065MPEQ5Hglo9Mo2BWBVaEPrZNEKyUBjbOMecehVqxu+YZ5LJTdydB6Xt+jzGZCA8TZvkItj56rsxCbuTohy1wj1MRF90gIIjgSEFB3xHofbyWtoJ/5g93sqrsA747wHiJCjeIuWnkG0nFGxKxk2e0IxKdkcOaXx8MIk8XoSJ6PB4/oLVCkUG4xY4Gt4zsKrloDp2oGCvVOconDJI6bxnD8QZ7CQqk95u8ZI3oE+OPYt wanghao@DESKTOP-SF37LJF
```

以后我们会用到这个文件里的内容去配置一些服务，你暂时只需要知道怎么生成这个 ssh-key 就行了。

## 用户

要注意的是，你生成的这个 ssh-key 只对你当前登录到系统上的这个用户有效。因为服务在验证你身份的时候，会检查你当前登录到系统上的这个用户的主目录下的 .ssh 里面的 ssh-key 。比如，你当前登录到系统上的用户名是 wanghao，他的 ssh-key 的位置应该是 `C:\Users\wanghao\.ssh`，macOS 上应该是 `/Users/wanghao/.ssh`。系统里的其他用户也应该在他的主目录下的 .ssh 目录里面有个 ssh-key，比如 xiaoxue，她的 ssh-key 的位置应该是 `C:\Users\xiaoxue\.ssh`，macOS 上应该是在 `/Users/xiaoxue/.ssh` 。

## 过程

下面是在 Windows 上使用 cmder 的 mintty 模式生成 ssh-key 的过程。

```
$ ssh-keygen

Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/wanghao/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/wanghao/.ssh/id_rsa.
Your public key has been saved in /c/Users/wanghao/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:3w9vT3YFRqrEqLcDNDq2Lep/F6i083wqZfP3usrkAFI wanghao@DESKTOP-SF37LJF
The key's randomart image is:
+---[RSA 2048]----+
|              .  |
|         o   o   |
|    E o . o . o  |
|   . o o . . . . |
|  . = o.S .     .|
|   o.==o.o .    .|
|   .o=oo+.. o   +|
|   .=o.=+..  +.o.|
| .o..=+++oo+..o..|

$ ls ~/.ssh
id_rsa  id_rsa.pub
```

---

1. [生成一对 ssh 密钥](https://ninghao.net/video/4572?a=51729)



