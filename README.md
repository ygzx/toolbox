# 小工具箱 · Toolbox

一个收纳自制小工具的纯静态网站。所有工具都是**单文件 HTML**，在浏览器本地运行，**不上传任何数据**，打开即用。

## ✨ 特性

- 纯前端，无后端、无构建步骤、无外部依赖
- 全部工具离线可用，数据不出本机
- 暗色主题，响应式布局
- 一键部署到 GitHub Pages（免费）

## 🧰 现有工具

| 工具 | 说明 | 路径 |
| --- | --- | --- |
| 图片压缩工具 | 拖入图片即可压缩，支持 JPEG / WebP / PNG，可调质量与尺寸，批量下载 | `tools/image-compressor.html` |

## 🚀 本地预览

直接用浏览器打开 `index.html` 即可；或在项目根目录起一个静态服务器：

```bash
# Python
python -m http.server 8000
# 然后访问 http://localhost:8000
```

## ➕ 添加新工具

1. 在 `tools/` 下新建一个单文件 HTML 工具（建议自带样式、无需联网）。
2. 在顶部加一个返回首页的导航条：
   ```html
   <div class="back-bar"><div class="container"><a href="../index.html">← 返回工具箱</a></div></div>
   ```
   并引入 `../assets/style.css` 中的 `.back-bar` 样式（或自带同等样式）。
3. 在 `index.html` 的 `.grid` 中复制一张卡片，填入名称、说明和链接。

## ☁️ 部署到 GitHub Pages

1. 把仓库推送到 GitHub。
2. 仓库 **Settings → Pages**，Source 选择 `Deploy from a branch`，分支选 `main`（或 `master`），目录选 `/ (root)`。
3. 保存后等待一两分钟，访问 `https://<用户名>.github.io/<仓库名>/`。

## 📄 License

MIT —— 随便用、随便改。
