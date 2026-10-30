# Jingyi Xu — Academic Homepage

Website: https://echo636.github.io
Repository: https://github.com/echo636/echo636.github.io

Built with [Academic Pages](https://github.com/academicpages/academicpages.github.io), based on Minimal Mistakes (MIT license). The original theme attribution and license are retained.

## 如何更新

直接在 GitHub 网页中打开对应文件，点击铅笔图标编辑并保存到 `master` 分支。GitHub Actions 会自动生成并发布网站，通常需要几分钟。

| 内容 | 文件 |
| --- | --- |
| 姓名、头像、学校、邮箱、学术链接 | `_config.yml` 中的 `author` |
| 个人简介、研究方向、动态 | `_pages/about.md` |
| 论文 | 在 `_publications/` 中添加 Markdown 文件 |
| 简历与经历 | `_pages/cv.md` |
| 顶部导航 | `_data/navigation.yml` |
| 照片 | 上传到 `images/`，然后修改 `_config.yml` 的 `author.avatar` |
| PDF 简历、论文附件 | 上传到 `files/` |

学校、身份、研究方向、邮箱、论文和经历目前均未填写。空白资料不会显示；示例人物、示例论文、示例简历及附件均已清除。当前头像仅为姓名首字母。

论文文件可命名为 `2026-01-01-short-title.md`。内容格式如下（请替换示例字段后再创建）：

```yaml
---
title: "论文标题"
collection: publications
category: conferences
permalink: /publication/short-title/
date: 2026-01-01
venue: "会议名称"
paperurl: "论文链接"
citation: "作者及引用信息"
---
论文简介。
```

期刊论文使用 `category: manuscripts`。CV 目前留空；上传 `files/cv.pdf` 后，可在 `_pages/cv.md` 中加入 `[Download CV](/files/cv.pdf)`。

## 发布设置

- 默认分支：`master`
- Settings → Pages → Source：`GitHub Actions`
- 发布流程：`.github/workflows/jekyll.yml`，直接沿用模板的构建流程
- 模板原有的 `Scrape Talk Locations` 和 `Cleanup bad PR` 工作流已在仓库中禁用
- 没有设置访问统计或评论系统

## 本地预览（可选）

需要 Ruby 3.1 或更新版本，以及 Node.js。

```sh
bundle config set --local path vendor/bundle
bundle install
npx --yes uglify-js assets/js/plugins/jquery.greedy-navigation.js assets/js/_main.js assets/js/theme.js -c -m -o assets/js/main.min.js
bundle exec jekyll serve
```

线上更新不需要在电脑上安装这些工具。请在仓库 Actions 页面查看发布是否成功。
