# 极简单页导航（Netlify版）

基于原 nav 项目修改前台 UI：去掉搜索框、导航图标和网站图标，改为浅薄荷绿/粉色背景、纯文字卡片；电脑端左侧分类栏，手机端自动隐藏侧栏并使用双列卡片布局。保留原项目的 Angular 路由和管理功能代码。

## Netlify 部署

1. 将本项目上传到自己的 GitHub 仓库。
2. 在 Netlify 选择 **Add new site → Import an existing project**，连接仓库。
3. Build command：`npm run build`
4. Publish directory：`dist`
5. Node 版本建议使用 18。
6. 点击 Deploy。

仓库已包含 `netlify.toml`，Netlify 通常会自动读取构建配置。

## 后台

原项目后台路由仍保留：网站部署后访问 `/#/system`。原项目的在线编辑/保存机制依赖原有的仓库授权配置，并不是 Netlify 自带数据库。若要让后台修改后自动保存到自己的仓库，需要按原项目说明配置仓库地址和对应访问凭据；请勿把有写权限的访问令牌提交到公开仓库。首次部署前建议在 Netlify 环境变量/项目配置中检查原项目授权设置。

## 本地构建

需要 Node.js 18：

```bash
npm install
npm run build
```

生成目录为 `dist`。
