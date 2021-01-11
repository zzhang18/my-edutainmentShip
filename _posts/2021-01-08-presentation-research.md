---
title: 开源ppt类工具研究
date: 2021-01-08 16:11:00 +0800
categories:
- learning
tags:
- utilities
- office
layout: post
toc: true
---

## 目的
寻找合适的原生ppt的展示，包含控制、播放ppt的，包括ppt的动画效果之类的项目作参考

## 思路要点
- 前端演示类PPT
  - 控制
  - 播放
  - 动画效果
- 功能（可能需要）
  - 编辑
  - 导入
  - 导出

## 方案参考
- [PptxGenJS](https://github.com/gitbrent/PptxGenJS)
  - 可npm调用，例如在react中引用模块
  - 代码生成ppt并点击下载pptx文档
- [reveal.js](https://github.com/hakimel/reveal.js)
  - 可npm调用，例如在react中引用模块
  - 使用markdown文件作为播放源（可外置）
  - 多主题支持
  - 可导出pdf



## 参考资料
* [PptxGenJS](https://github.com/gitbrent/PptxGenJS)
* [GitHub 标星 54K + 2K！这才是程序员写逼格满满的 PPT 的正确姿势！](https://segmentfault.com/a/1190000038407989)
* [reveal.js](https://github.com/hakimel/reveal.js)
* [slides](https://slides.com/)