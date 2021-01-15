---
title: 飞书小程序入门
date: 2021-01-12 17:11:00 +0800
categories:
- learning
tags:
- utilities
layout: post
toc: true
---

## 目的
入门飞书小程序的开发和发布，功能需求是打开即能带用户认证的跳转会议链接的飞书PC端小程序。


## 流程
1. 按照[官方教程](https://open.feishu.cn/document/uQjL04CN/ukjL54SO)文档指引，安装开发者工具。（英文教程提示安装VSCode插件，中文教程提示使用cli组件）
2. 进入[飞书开放平台](https://open.feishu.cn/app/)创建APP
3. 初始化项目并关联APP ID
4. 配置[AppLink 协议](https://open.feishu.cn/document/uYjL24iN/ucjN1UjL3YTN14yN2UTN)并将各参数代入链接，例如我的APP ID是cli_9f77f74a9976500b，代入会议参数为meetingId 那么打开链接即为 https://applink.feishu.cn/client/mini_program/open?appId=cli_9f77f74a9976500b&mode=window&bdp_launch_query=meetingId
5. 获取链接参数[getHostLaunchQuery](https://open.feishu.cn/document/uYjL24iN/ugzM4UjL4MDO14COzgTN)
```js
tt.getHostLaunchQuery({
    success (res) {
        console.log(`传入的参数为 ${res.launchQuery}`);
    },
    fail (res) {
        console.log(`获取传入的参数失败`);
    }
});
```
6. 获取用户信息[getUserInfo](https://open.feishu.cn/document/uYjL24iN/ucjMx4yNyEjL3ITM)
```js
tt.getUserInfo({
    success (res) {
        console.log(`getUserInfo 调用成功 ${res.userInfo}`);
    },
    fail (res) {
        console.log(`getUserInfo 调用失败`);
    }
});
```
7. 跳转网页[openSchema](https://open.feishu.cn/document/uYjL24iN/ukzN4IjL5cDOy4SO3gjM) 
```js
tt.openSchema({
    schema: 'https://www.apple.com',
    external: false,
    success (res) {
        console.log(`${res}`);
    },
    fail (res) {
        console.log(`open fail`);
    }
});
```
8. 打包上传并发布小程序后打开4中的链接测试验证

## 注意事项
- 飞书开发者工具目前仅支持登录公有云版飞书创建上传小程序，私有云需定制化开发者工具
- 小程序内数据请求为异步请求，有些步骤需得到返回值后再进行下一步

## 参考资料
- [官方教程](https://open.feishu.cn/document/uQjL04CN/ukjL54SO)






