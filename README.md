# 简相册 · 产品介绍与法律文本 / Simple Album · Landing & Legal

本仓库存放 **简相册（Simple Album）** iOS App 的产品介绍页与法律文本页，用于 App Store 上架（Marketing / Support URL）与用户查阅。
This repository hosts the product landing page and legal pages for the Simple Album iOS app.

线上地址 / Live site：<https://hustliweizeng.github.io/keepsake-legal/>

## 页面 / Pages

| 页面 | Page | 线上路径 |
|---|---|---|
| `index.html` | 产品介绍页（中英双语单页） | `/` |
| `legal.html` | 法律文本中转页（中英四入口） | `/legal.html` |
| `privacy.html` | 隐私政策（中文） | `/privacy.html` |
| `privacy-en.html` | Privacy Policy | `/privacy-en.html` |
| `support.html` | 支持与常见问题（中文） | `/support.html` |
| `support-en.html` | Support & FAQ | `/support-en.html` |

## 技术说明 / Notes

- 纯静态：无构建步骤、无依赖、无外链 CSS / 字体 / 脚本
- 无 Cookie、无追踪、无统计、无第三方请求
- 产品页为单文件单页：中英切换靠 `lang-zh` / `lang-en` 类名，图形示意全部内联 SVG / CSS，不用真机截图
- 法律页中文优先，页面顶部提供中英切换；支持深色模式（`prefers-color-scheme`）
- `.nojekyll` 用于跳过 GitHub Pages 的 Jekyll 处理

改内容直接编辑对应 HTML 推送到 `main`，Pages 会在 1 分钟内自动重新部署。

> 产品页的可编辑母本在仓库外 `../product-site/index.html`（那里用的是绝对链接，方便单独预览）；
> 发布到本仓库后链接已改成相对路径，**改完记得同步回母本**，或直接以本仓库版本为准。
