---
title: Clarity v1.3.0 版本更新日志
date: 2025-05-09 11:27:40
categories:
  - 版本日志
tags:
  - clarity
---

v1.3.0 正式发布啦~

## Config

主题配置文件有一些改动，下面是改动详情。（- 表示删除的行，+表示新增的行）

1. waline 添加 reaction 选项，可以关闭评论区上边的反应表情了。 

```diff
waline: 
...
  wordLimit: 500 
+  reaction: true ## Whether to show reaction emoji list
  requiredMeta: ['nick','mail']
...
```

2. 不蒜子 添加站点统计功能。

```diff
-busuanzi: false ## If you want to use Busuanzi page views please set the value to true.
+busuanzi: ## Busuanzi statistic
+  site_enable: true ## Whether to enable site statistic.
+  post_enable: false ## Whether to enable post statistic.
```

3. 可以开关 Open Graph 内容了。 

```diff
site_bg_img:

+post_meta:
+  open_graph: true # Whether to enable Open Graph.
```

4. 侧边栏 个人信息区 添加 Follow 按钮（可关闭）。

```diff
info:
  avatar: /img/avatar.png
  discription: To be a better man.
+  follow:
+    enable: true
+    icon: fa fa-github
+    text: Follow Me
+    link: https://github.com/username
```

## Features

- feat: enable Open Graph or not
- fix: 侧边栏链接改为使用配置信息拼接
- feat: 侧边栏个人信息处新增可关闭的 Follow 按钮
- feat: waline 添加表情互动开关配置、浏览量统计
- feat: 添加不蒜子站点统计
- refactor: 调整页面结构，样式和脚本分离，提升性能
- refactor: 页脚在底部居中



