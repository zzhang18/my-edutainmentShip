---
title: 无线联网门锁云服务平台
date: 2021-01-25 17:15:00 +0800
categories:
- learning
tags:
- ELE
layout: post
toc: true
---

## 目的
熟悉并测试智能门锁LMS-B2

## 材料清单
1. 智能门锁LMS-B2-V1.2（4节五号电池）
2. 两脚插头无线主控器，型号CBW1-04，ID：16064002277C，S/N：01061606S506000330000070
3. 主控器电源，型号MH-050200，输入100-240V/50-60Hz/0.5A，输出5VDC/2A
4. 三角插头电源适配器，型号YU1205，输入AC100-240V1.8A 50-60Hz，输出DC12V——5A
5. 云服务平台WebService接口文档（2.8版本）

## 思路
1. 按照型号搜索官网，可得[网址](http://www.enginhz.com/productdetails/13.html)
   1. 智能门锁 LMS-B2：无线联网模块集成在智能锁内，采用非接触感应卡开锁方式，使用四节5号电池或充电电池工作，可持续开关30000次以上，紧急情况可使用钥匙开锁。LMS系列适合于木门安装，有80万次以上的锁舌使用寿命。
   2. 门锁与主控器通讯距离：建议＜5米(无遮挡)
   3. RFID卡类型：Mifare One/cpu卡/身份证/居住证等
   4. 开门模式：刷卡开门、远程开门、遥控器开门、机械钥匙等
   5. 供电：四节5号碱性电池
   6. 电池平均使用寿命：每天20次刷卡，可使用1年以上
   7. 开门响应时间：平均约为0.5秒
   8. 提示音：多种音乐提示
   9. 指示灯：运行、电池低压告警指示
   10. 电池电压监测：中心实时显示门锁电池电压,低电压时在门锁及中心均有声音和指示灯告警
   11. 刷卡认证：锁内已存储卡数据认证，设备脱机不影响正常进出门
   12. 门锁状态信息发送：刷卡信息、开关门状态信息、保险状态以及电池电量信息、无线信号强度信息
   13. 脱机刷卡记录：200条
   14. 锁内权限数量：1000人
2. 尝试进[登录系统](https://cloud.enginhz.com/apartment/login),报错

```
Whitelabel Error Page
This application has no explicit mapping for /error, so you are seeing this as a fallback.

Mon Jan 25 17:24:27 CST 2021
There was an unexpected error (type=Internal Server Error, status=500).
Connect to 172.16.102.142:8082 [/172.16.102.142] failed: Connection refused (Connection refused)
```

## 参考资料
- [智能门锁LMS-B2官方文档](http://www.enginhz.com/productdetails/13.html)





