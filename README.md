# 柒月博客 - 部署指南

## ✅ 已完成

1. ✅ GitHub 仓库已创建: `gaoxuwu2000/qiyue-blog`
2. ✅ Hexo 博客框架已安装
3. ✅ Butterfly 主题已安装并配置
4. ✅ 初始化文章（欢迎页、关于、友链）
5. ✅ 部署配置文件已推送

---

## 🚀 下一步：连接 Vercel

### 方法一：手动连接（最简单，推荐）

1. 打开 👉 https://vercel.com/new
2. 点击 **Import Git Repository**
3. 选择 `gaoxuwu2000/qiyue-blog`
4. Vercel 会自动识别 `vercel.json`，无需任何配置
5. 点击 **Deploy**，等待 ~2 分钟
6. 获得博客地址：`xxxx.vercel.app`

### 方法二：命令行部署（需要 Vercel 账号）

```bash
# 安装 Vercel CLI
npm install -g vercel

# 登录
vercel login

# 进入博客目录
cd qiyue-blog

# 部署（首次会交互式提问）
vercel

# 正式上线
vercel --prod
```

---

## 🔧 自定义域名（可选）

部署成功后，可以在 Vercel 控制台绑定自己的域名（如 `blog.yourname.com`）

---

## 📝 写文章方法

博客目录: `C:\Users\Administrator\.qclaw\workspace\qiyue-blog\source\_posts\`

创建新文章：
```markdown
---
title: 文章标题
date: 2026-04-15
categories:
  - 分类
tags:
  - 标签
---

正文内容...

<!-- more -->  <!-- 摘要截断符 -->

正文继续...
```

写完后推送到 GitHub，Vercel 会自动重新部署。

---

## 📁 博客目录结构

```
qiyue-blog/
├── source/
│   └── _posts/          ← 文章放这里
│   ├── about/           ← 关于页面
│   └── link/            ← 友链页面
├── themes/
│   └── butterfly/       ← 主题配置
│       └── _config.yml  ← 修改主题外观
├── _config.yml          ← 博客主配置
└── vercel.json          ← Vercel 配置文件
```