# 留真的法律文本页（隐私政策 / 支持）

这 5 个文件是**自包含**的静态页：没有外链 CSS、没有字体请求、没有第三方脚本、没有 Cookie、没有追踪。
丢到任何静态主机上都能直接跑，不需要构建。

| 文件 | 内容 | 线上路径 |
|---|---|---|
| `index.html` | 中转页（中英四入口） | `/` |
| `privacy.html` | 隐私政策（中文） | `/privacy.html` |
| `privacy-en.html` | Privacy Policy | `/privacy-en.html` |
| `support.html` | 支持与常见问题（中文） | `/support.html` |
| `support-en.html` | Support & FAQ | `/support-en.html` |
| `.nojekyll` | 让 GitHub Pages 跳过 Jekyll（否则下划线开头的文件会被吞） | — |

---

## 方式 A · GitHub Pages（推荐，免费且不需要 ICP 备案）

### 为什么必须单独建一个仓库

当前 `hustliweizeng/photoManager` 是**私有仓库**（未登录访问返回 404）。两个后果：

1. 私有仓库开 Pages 需要 **GitHub Pro**；
2. 更重要的：把整仓公开，等于把扫描算法、设计文档、决策记录一起公开了 —— 没必要。

所以只把**这 5 个静态文件**放进一个新的公开仓库。

### 步骤

1. 在 GitHub 网页上新建仓库：名字 **`keepsake-legal`**、**Public**、**不要**勾 README（保持空仓）
2. 然后在本机执行：

```bash
cd ~/WorkBuddy/photoManager/legal-site
git init
git add -A
git commit -m "docs: 留真隐私政策与支持页（中英）"
git branch -M main
git remote add origin git@github.com:hustliweizeng/keepsake-legal.git
git push -u origin main
```

3. 打开仓库 → **Settings → Pages** → Source 选 **Deploy from a branch**
   → 分支 **main**、目录 **/(root)** → **Save**
4. 等 1–2 分钟，访问 `https://hustliweizeng.github.io/keepsake-legal/`
   四个子页分别是 `/privacy.html`、`/privacy-en.html`、`/support.html`、`/support-en.html`

### 填进 App Store Connect 的两个网址

| ASC 字段 | 填 |
|---|---|
| 隐私政策网址 | `https://hustliweizeng.github.io/keepsake-legal/privacy.html` |
| 支持网址 | `https://hustliweizeng.github.io/keepsake-legal/support.html` |

> 这两个字段 Apple **会真的打开**。要点：必须是 https、公开可访问、不需要登录、正文里能看到
> "收集什么数据"和"联系方式"。本项目是"不收集任何数据"，页面已按这个口径写。
> 中文页给中国区审核用，英文页作为补充；两个网址都填中文那份即可（审核员看英文版可点页面顶部的 English）。

---

## 方式 B · 已有域名（我已验证可用，一条命令就能上线）

`https://keepsake-ota.app.workbuddy.host/` 这个静态站已经在跑（现在放的是内测安装页）。
把本目录发上去，同一套文件就能用，并且**国内访问比 github.io 稳**。

---

## 两条实话（发布前值得知道）

1. **GitHub 在中国大陆访问不稳定。** Apple 审核员在境外，通常能打开，所以不会因此被拒；
   但中国区用户点"隐私政策"可能转圈。若在意，用方式 B，或两个都发、ASC 填国内可达的那个。
2. **GitHub Pages 的 `github.io` 域名已被大量滥用**，个别网络环境下会被整体屏蔽。
   Apple 只要求"公开可访问"，但审核那一刻打不开就会被打回 —— 这是唯一需要在意的风险。
