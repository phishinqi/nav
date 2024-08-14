## 部署

零成本部署，像数 `321` 一样简单。

#### gh-pages (免费)

1、右上角点击 `Fork` 当前项目。

2、[https://github.com/settings/tokens/new](https://github.com/settings/tokens/new) 申请 `token`, 勾选相应的权限, 如果不懂就全部选中，复制并保存 Token；[Gitee 申请点这里](https://gitee.com/profile/personal_access_tokens/new)

3、https://github.com/你的用户名/nav/settings/secrets/actions/new 添加申请的 token， name 填写 `TOKEN` 大写。

4、打开 https://github.com/你的用户名/nav/actions 开启 action 自动部署

5、修改项目根目录配置文件 [nav.config.ts](nav.config.ts) 只需要修改仓库地址

6、打开 https://你的用户名.github.io/nav 就能看到一个非常强大的导航网站了。

#### Netlify 推荐(免费)

作者目前使用，速度较快

[https://www.netlify.com/](https://www.netlify.com/)

#### Vercel 推荐(免费)

国内访问速度较慢，建议测试后使用

[https://github.com/apps/vercel](https://github.com/apps/vercel)

#### 关于自有部署

前提服务器必须能访问公网。(内网收益太小，暂时不加入需求，有需要的可以众筹) 也可以将仓库设为私有

将代码拉到服务器 `git clone https://github.com/xjh22222228/nav.git` 还需要安装`Node >= 18`

执行 `npm i && npm run build`

```bash
# 启动 公网IP:7777, 后台系统配置请求地址填写：公网IP:7777/server
npm run server
```

#### 其他

如果您有更好的部署方式，请给我们提 PR

## 后台

将路由地址修改为 `system` 即可进入，如: https://www.nav3.cn/#/light 修改为 https://www.nav3.cn/#/system

## 升级

将你的仓库克隆下来执行以下命令

```bash
git pull
git remote add upstream https://gitee.com/xiejiahe/nav.git
git fetch upstream main
git merge upstream/main --allow-unrelated-histories --no-edit
git push

# 如果安装了node只需执行
npm run update
```

## 更新日志

[CHANGELOG](https://github.com/xjh22222228/nav/releases)

## 开发构建

NODE: >= v18

```bash
# 下载
git clone --depth=1 https://github.com/xjh22222228/nav.git

cd nav

# 安装依赖 NODE: v18
yarn

# 启动
yarn start

# 打包
yarn build
```

## 建议

如果有任何功能上的建议可通过 [issue](https://github.com/xjh22222228/nav/issues) 发起, Thank you.

## 支持

项目于 2018 年到至今一直坚持维护和开源, 经过 N 次的迭代与优化, 如果项目能帮到您是我的荣幸。

您可以请作者喝杯咖啡，继续战斗下去（请备注 Github 名字）~

<img src="https://cdn.jsdelivr.net/gh/xjh22222228/public@gh-pages/img/32.png" width="600">

<img src="https://cdn.jsdelivr.net/gh/xjh22222228/public@gh-pages/nav/thank.png" width="200" />

## License

[MIT](./LICENSE)
