# 留真 · 隐私政策与支持 / Keepsake · Privacy & Support

本仓库只存放 **留真（Keepsake）** iOS App 的法律文本页，用于 App Store 审核与用户查阅。
This repository only hosts the legal pages for the Keepsake iOS app.

线上地址 / Live site：<https://hustliweizeng.github.io/keepsake-legal/>

## 页面 / Pages

| 页面 | Page | 线上路径 |
|---|---|---|
| `index.html` | 中转页（中英四入口） | `/` |
| `privacy.html` | 隐私政策（中文） | `/privacy.html` |
| `privacy-en.html` | Privacy Policy | `/privacy-en.html` |
| `support.html` | 支持与常见问题（中文） | `/support.html` |
| `support-en.html` | Support & FAQ | `/support-en.html` |

## 技术说明 / Notes

- 纯静态：无构建步骤、无依赖、无外链 CSS / 字体 / 脚本
- 无 Cookie、无追踪、无统计、无第三方请求（页面上唯一的外部链接是 `mailto:`）
- 中文优先，页面顶部提供中英切换；支持深色模式（`prefers-color-scheme`）
- `.nojekyll` 用于跳过 GitHub Pages 的 Jekyll 处理

改内容直接编辑对应 HTML 推送到 `main`，Pages 会在 1 分钟内自动重新部署。
