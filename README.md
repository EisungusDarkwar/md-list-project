
# 📝 Markdown 卡片列表项目

一个基于 Astro 构建的轻量级 Markdown 文章管理系统，支持卡片式列表展示、实时搜索和响应式布局。

## ✨ 功能特性

- 📄 **Markdown 支持** - 自动读取并渲染 Markdown 文件
- 🎴 **卡片式布局** - 美观的响应式卡片网格展示
- 🔍 **实时搜索** - 根据标题和描述快速过滤文章
- 📱 **响应式设计** - 完美适配 PC、平板和手机
- 🚀 **高性能** - Astro 静态生成，首屏加载极快
- 🎨 **美观 UI** - 渐变背景、卡片悬停动画效果

## 🛠️ 技术栈

- [Astro](https://astro.build/) - 静态站点生成器
- Markdown - 内容管理
- CSS3 - 样式设计（无框架依赖）

## 📁 项目结构

md-list-project/
├── src/
│ ├── pages/
│ │ ├── index.astro # 首页（卡片列表）
│ │ └── posts/
│ │ └── [...slug].astro # 动态路由（文章详情）
│ ├── posts/ # Markdown 文章目录
│ │ ├── 第一篇文章.md
│ │ ├── 第二篇文章.md
│ │ └── 第三篇文章.md
│ ├── layouts/
│ │ └── Layout.astro # 全局布局组件
│ └── utils/
│ └── date.js # 日期格式化工具
├── public/
│ └── style.css # 全局样式
├── package.json
└── README.md
text


## 🚀 快速开始

### 环境要求

- Node.js 18.0 或更高版本
- npm 或 yarn 或 pnpm

### 安装步骤

1. **克隆项目**
```bash
git clone <your-repo-url>
cd md-list-project

    安装依赖

bash

npm install

    启动开发服务器

bash

npm run dev

    访问项目
    打开浏览器访问 http://localhost:4321

📝 添加文章

在 src/posts/ 目录下创建 .md 文件，格式如下：
markdown

---
title: "文章标题"
description: "文章简短描述"
date: "2024-01-15T14:30:00+08:00"
slug: "custom-url-slug"  # 可选，用于自定义 URL
---

# 文章标题

这里是文章内容，支持 **Markdown** 语法。

- 列表项 1
- 列表项 2

> 引用内容

[链接文字](https://example.com)

Frontmatter 字段说明
字段	必填	说明	示例
title	✅	文章标题	"我的第一篇文章"
description	✅	文章描述	"这是一篇介绍文章"
date	✅	发布日期	"2024-01-15T14:30:00+08:00"
slug	❌	自定义URL	"my-first-post"
🔧 构建与部署
构建生产版本
bash

npm run build

构建产物会生成在 dist/ 目录。
预览生产版本
bash

npm run preview

部署到服务器

将 dist/ 目录下的所有文件上传到你的 Web 服务器即可。
推荐部署平台

    Vercel

bash

npm install -g vercel
vercel

    Netlify

bash

npm install -g netlify-cli
netlify deploy

    GitHub Pages

bash

npm run build
# 将 dist 目录推送到 gh-pages 分支

📖 使用指南
搜索功能

点击顶部的搜索框，输入关键词即可实时过滤文章。搜索范围包括：

    文章标题

    文章描述

阅读文章

点击任意卡片即可进入文章详情页，支持完整的 Markdown 渲染。
返回首页

在文章详情页点击"← 返回列表"链接即可回到首页。
🎨 自定义样式

修改 public/style.css 文件来自定义样式：
css

/* 修改主题色 */
.card-title {
  color: #your-color;  /* 修改标题颜色 */
}

/* 修改背景渐变 */
body {
  background: linear-gradient(135deg, #your-color1, #your-color2);
}

📄 时间格式说明

项目支持多种时间格式，推荐使用 ISO 8601 标准格式：
yaml

# 推荐格式（包含时区）
date: "2024-01-15T14:30:00+08:00"

# 也支持以下格式
date: "2024-01-15 14:30:00"
date: "2024-01-15"

🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

    Fork 本仓库

    创建特性分支 (git checkout -b feature/AmazingFeature)

    提交更改 (git commit -m 'Add some AmazingFeature')

    推送到分支 (git push origin feature/AmazingFeature)

    开启 Pull Request

📝 更新日志
v1.0.0 (2024-01-15)

    ✨ 初始版本发布

    🎴 实现卡片式列表布局

    🔍 添加实时搜索功能

    📱 实现响应式设计

    📄 支持 Markdown 文件渲染

📄 许可证

本项目采用 MIT 许可证，详情请查看 LICENSE 文件。
🙏 致谢

    Astro - 优秀的静态站点生成器

    Markdown - 简洁的内容编写格式

📧 联系方式

如有问题或建议，欢迎通过以下方式联系：

    提交 Issue

    发送邮件至 [your-email@example.com]

⭐ Star 历史

如果这个项目对你有帮助，欢迎给个 Star！⭐
text


## 同时创建一个 .gitignore 文件

**.gitignore**
```gitignore
# 依赖
node_modules/
package-lock.json
yarn.lock
pnpm-lock.yaml

# 构建产物
dist/
.astro/

# 环境变量
.env
.env.local
.env.*.local

# 编辑器
.vscode/
.idea/
*.swp
*.swo
*~

# 系统文件
.DS_Store
Thumbs.db

# 日志
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*

创建简单的 LICENSE 文件（MIT 许可证）

LICENSE
text

MIT License

Copyright (c) 2024 [你的名字]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

创建 package.json（如果还没有）

package.json
json

{
  "name": "md-list-project",
  "type": "module",
  "version": "1.0.0",
  "description": "一个基于 Astro 的 Markdown 卡片列表项目",
  "author": "你的名字",
  "license": "MIT",
  "scripts": {
    "dev": "astro dev --host",
    "start": "astro dev",
    "build": "astro build",
    "preview": "astro preview --host",
    "astro": "astro"
  },
  "dependencies": {
    "astro": "^4.0.0"
  },
  "keywords": [
    "astro",
    "markdown",
    "blog",
    "static-site"
  ],
  "repository": {
    "type": "git",
    "url": "git+https://github.com/你的用户名/md-list-project.git"
  },
  "bugs": {
    "url": "https://github.com/你的用户名/md-list-project/issues"
  },
  "homepage": "https://github.com/你的用户名/md-list-project#readme"
}
