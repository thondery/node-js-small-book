# 基本使用

### 1. 创建项目

```bash
# 创建目录
$ mkdir my-project && my-project

# 初始化项目
$ npm init
Or
$ yarn init
```

### 2. 安装 npm 包

全局安装

```bash
$ npm i -g <package-name>
or
$ yarn add global <package-name>
```

本地安装

```bash
$ npm i <package-name>

# 安装并写入 package.json 的 dependencies
$ npm i --save <package-name>
$ yarn add <package-name>

# 安装并写入 package.json 的 devDependencies
$ npm i --save-dev <package-name>
$ yarn add -D <package-name>

# 安装 package.json 里所有的包
$ npm i
or
$ yarn

# 更新 package.json 里所有的包
$ rm -rf node_modules && npm i
or
$ yarn upgrade

# 删除包
$ npm uninstall <package-name>
or
$ yarn remove <package-name>

# 清除缓存
$ npm cache clean
or
$ yarn cache clean
```

package-name

| package-name | 说明 |
|--------------|-----|
| package-name | 安装 latest 最新版本 |
| package-name@1.0.0 | 安装指定版本 |
| package-name@next | 安装指定 tag 版本 |
| git remote url | 从远程 git repo 里安装 |
| file:/path/to/local/folder | 从本地目录里安装 |
| file:/path/to/local/tarball.tgz | 从本地压缩包里安装 |

### 3. 发布 npm 包

存储 npm registry 的 authToken

```bash
$ npm adduser --registry=https://registry.npmjs.org
Username:
Password:
Email:
```

删除 npm registry 的 authToken

```bash
$ npm logout --registry=https://registry.npmjs.org
```

发布

```bash
$ npm publish  # 默认发布
$ npm publish --tag next # 发布到指定 tag
$ npm unpublish <package-name>@<version>  # 删除已发布的包
```

注：官方只允许删除发布未超过24小时的包，如果你真要删除需通过 <support@npmjs.com> 进行联系