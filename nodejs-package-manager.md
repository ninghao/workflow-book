# Node.js 包管理

把用 Node.js 做好的某个功能打成一个包（Package），在项目之间可以重复使用这些包。即使你开发的不是 Node.js 项目，也可能会用到 Node.js 的某些包。特别是做前端项目开发的时候，项目里用的很多工具都是 Node.js 的一个包。

这些 Node.js 的包之间会存在依赖关系，也就是一个包的功能，可能需要另一个包里提供的功能。Node.js 让你可以在项目里使用一个叫 package.json 的文件去描述包的依赖关系，使用工具，执行一行命令就可以安装项目需要的所有的包。这个工具会为你解决包之间的依赖关系。

有的包可以在服务端使用，有些是命令行工具，也有很多包可以用在前端，也就是直接在浏览器上去用。在你的项目里去，可以直接使用一些现成的包。你也可以创建自己的包，跟别人共享，或者只在自己团队的内部使用。

在项目里管理 Node.js 的包可以使用 npm 或 yarn。

## npm

npm（Node Package Manager），是一个包管理工具。安装了 Node.js 以后，会自带这个包管理工具。

[https://www.npmjs.com/](https://www.npmjs.com/)

### Yarn

Yarn 是可以代替 npm 的又一个 Node.js 包管理工具，它比 npm 更快更安全。

[https://yarnpkg.com](https://yarnpkg.com)

