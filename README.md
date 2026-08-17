# 我的小博客 📝

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

1. **在 GitHub 上新建一个仓库**，名字随意（例如 `my-blog`），保持公开。
2. **把本项目推送到仓库**：

   ```bash
   git init -b main
   git add .
   git commit -m "first commit"
   git remote add origin https://github.com/你的用户名/my-blog.git
   git push -u origin main
   ```

3. **开启 GitHub Pages**：
   - 仓库页面 → `Settings` → `Pages`
   - `Build and deployment` → `Source` 选择 **GitHub Actions**
   - 仓库里已经带好了自动部署工作流（`.github/workflows/hugo.yaml`），推送后会自动构建并发布

发布完成后，你的博客地址是：`https://你的用户名.github.io/my-blog/`

## 别忘了改这些

- `hugo.toml` 里的 `baseURL`（改成你的真实地址）
- `hugo.toml` 里的 `YOUR-USERNAME`（社交链接）
- 想用自定义域名？在仓库 `Settings → Pages` 里设置即可

## 写新文章

```bash
hugo new content posts/我的新文章.md
```

写好 Markdown 内容后保存，推送到 GitHub 就会自动发布。
