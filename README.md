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
