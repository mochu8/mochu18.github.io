# mochu8.github.io

这是 [mochu8 的技术博客](https://mochu8.github.io/)，用于记录编程学习、工具实践和网站维护过程。

站点使用 Jekyll 构建，由 GitHub Pages 从 `master` 分支自动发布。

## 在线访问

- 博客首页：[https://mochu8.github.io/](https://mochu8.github.io/)
- 项目页面：[https://mochu8.github.io/projects.html](https://mochu8.github.io/projects.html)
- Telegram 机器人工具箱：[https://mochu8.github.io/telegram-tools.html](https://mochu8.github.io/telegram-tools.html)

## 当前特性

- 文章、标签、分类和项目页面
- 响应式侧边栏与移动端导航
- Atom 订阅、站点地图和 SEO 元数据
- 本地托管的文章图片与前端资源
- 无第三方统计、评论和社交展示脚本
- 无依赖的 Telegram Bot 辅助工具

## 项目结构

```text
.
|-- _config.yml       # Jekyll 与站点配置
|-- _posts/           # 已发布文章
|-- _drafts/          # 未发布草稿
|-- _layouts/         # 页面布局
|-- _includes/        # 可复用模板
|-- categories/       # 分类索引
|-- tags/             # 标签索引
|-- public/           # 样式、脚本、字体与图片
|-- about.md          # 关于页面
|-- links.md          # 项目页面
`-- telegram-tools.html
```

## 本地运行

需要安装 Ruby、Bundler 和 Git。

```bash
git clone https://github.com/mochu8/mochu8.github.io.git
cd mochu8.github.io
bundle install
bundle exec jekyll serve
```

启动后访问 [http://127.0.0.1:4000/](http://127.0.0.1:4000/)。

## 新增文章

在 `_posts/` 中创建符合 `YYYY-MM-DD-slug.md` 格式的文件：

```yaml
---
layout: post
title: 文章标题
date: 2026-07-24 20:00:00 +0800
categories: [站点]
tags: ["GitHub Pages", "Jekyll"]
---
```

正文使用 Markdown。站内资源通过 Jekyll 的 `relative_url` 过滤器引用：

```liquid
![图片说明]({{ "/public/images/mountains.jpg" | relative_url }})
```

提交并推送到 `master` 后，GitHub Pages 会自动构建和发布。

## 内容归属

当前仓库由开源 Jekyll 项目整理而来。历史文章中的作者表述、项目链接和引用按原文保留；后续新增内容由 `mochu8` 维护。

## 许可

站点模板代码遵循 [MIT License](LICENSE)。历史文章及其引用遵循各自原有许可和署名要求。
