---
title: 飞书消息推送
date: 2021-01-22 16:23:00 +0800
categories:
- learning
tags:
- utilities
layout: post
toc: true
---

## 目的
为飞书用户推送预订会议信息和链接寻找解决方案。


## 方案1 订阅事件——小程序机器人应用群发
- 进入[开发者后台](https://open.feishu.cn/app/)，选择应用
- 点击事件订阅，填入公网请求地址URL
- 选择监听事件
- 群发消息
   
## 方案2 飞书捷径——自定义机器人发送消息
- 进入[飞书管理后台-应用列表-飞书捷径](https://oda17oet1d.feishu.cn/admin/appCenter/manage/cli_9c2e4621576f1101)
- 应用编辑：选择应用，配置触发器，填写Webhook地址
- 飞书消息：选择飞书消息，自定义机器人发送消息，设置选项
- 触发消息发送


## 参考资料
- [批量发送消息](https://open.feishu.cn/document/ukTMukTMukTM/ucDO1EjL3gTNx4yN4UTM)
- [开发机器人应用](https://open.feishu.cn/document/uQjL04CN/uYTMuYTMuYTM)
- [订阅事件](https://open.feishu.cn/document/ukTMukTMukTM/uUTNz4SN1MjL1UzM#%E8%AF%B7%E6%B1%82%E7%BD%91%E5%9D%80)






