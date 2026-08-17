# 知微录 📝

用 **Hugo + PaperMod** 搭建的静态博客，托管在 GitHub Pages（免费）。

## 功能

- 🏠 首页欢迎区 + 文章列表
- 🌙 明暗主题自动切换
- 🔍 站内全文搜索（Fuse.js，无需后端）
- 📐 LaTeX 数学公式（MathJax 3）
- 💻 代码高亮 + 一键复制按钮
- 🏷️ 标签、🗂️ 归档、📡 RSS 订阅

## 本地预览

```bash
hugo server -D
```

浏览器打开 <http://localhost:1313> 即可预览。

## 发布到 GitHub Pages（3 步）

1. **在 GitHub 上新建仓库**，名字填 `jinhuaiqun.github.io`（必须和你的用户名一致），选择 **Public**。
2. **把本项目推送到仓库**（Git 会弹出登录窗口，用浏览器登录一次即可）：

   ```bash
   git push -u origin main
   ```

3. **开启 GitHub Pages**：
   - 仓库页面 → `Settings` → `Pages`
   - `Build and deployment` → `Source` 选择 **GitHub Actions**
   - 仓库里已经带好了自动部署工作流（`.github/workflows/hugo.yaml`），推送后会自动构建并发布

发布完成后，你的博客地址是：`https://jinhuaiqun.github.io/`

## 别忘了改这些

- `hugo.toml` 里的 `YOUR-USERNAME`（社交图标链接，改成你的 GitHub 用户名）
- `hugo.toml` 里的 `you@example.com`（改成你的邮箱）
- **不用改 `baseURL`**：本地预览用它指向 `localhost:1313`，部署时工作流会自动覆盖成你的真实网址
- 想用自定义域名？在仓库 `Settings → Pages` 里设置即可（此时才需要把 `baseURL` 改成你的域名）

## 写新文章

```bash
hugo new content posts/我的新文章.md
```

写好 Markdown 内容后保存，推送到 GitHub 就会自动发布。
