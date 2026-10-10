# my-vuepress-site

网站使用 [vuepress](https://vuepress.vuejs.org/) 和 [vuepress-theme-plume](https://github.com/pengzhanbo/vuepress-theme-plume) 构建生成。

## Install

```sh
npm install
```

## Usage

```sh
# 启动开发服务
npm run docs:dev
# 构建生产包
npm run docs:build
# 本地预览生产服务
npm run docs:preview
# 更新 vuepress 和主题
npm run vp-update
```

## 部署到 GitHub Pages

`docs` 是 VuePress 源文件目录，需要构建后发布，不能直接将源码目录当作静态网站发布。

1. 在 GitHub 仓库的 **Settings → Pages → Build and deployment** 中，将 **Source** 设置为 **GitHub Actions**。
2. 将本项目（包括 `.github/workflows/deploy-pages.yml`）推送到 `main` 分支。
3. 在仓库 **Actions** 页面等待 **Deploy VuePress to GitHub Pages** 完成，也可以通过 **Run workflow** 手动触发。
4. 访问 https://MrEverestChen.github.io/。

部署流程会安装依赖、执行 `npm run docs:build`，并发布 `docs/.vuepress/dist`。后续将文章修改推送到 `main` 后会自动更新网站。

当前仓库为用户站点 `MrEverestChen.github.io`，因此 `docs/.vuepress/config.ts` 中的 `base` 应保持为 `/`。

## 参考文档

- [vuepress](https://vuepress.vuejs.org/)
- [vuepress-theme-plume](https://theme-plume.vuejs.press/)
