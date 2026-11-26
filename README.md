# Plum Jam's Blog

基于 Jekyll 的个人博客，托管在 GitHub Pages。

## 本地预览（可选）

如果安装了 Ruby，可以本地预览：

```bash
gem install jekyll bundler
bundle exec jekyll serve
```

然后访问 http://127.0.0.1:4000

## 发布

推送到 GitHub 的 `main` 分支即可自动构建发布：

```bash
git add .
git commit -m "update"
git push origin main
```

## 写新文章

在 `_posts` 目录下创建 `YYYY-MM-DD-标题.md` 文件，参考已有文章格式。