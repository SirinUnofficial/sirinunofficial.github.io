---
title: 6.创建爆炸
author: Sycamore0
date: 2025-03-01 23:16:00 +0800
categories: [简体中文, 我的幸运方块
tags: [我的幸运方块]
---

# 创建爆炸create_explosions

> 本条目基于MyLuckyBlock 1.2.0版本
{: .prompt-tip }

> 条目需要完善
{: .prompt-info }

## 基本
- `power` [int]爆炸强度(默认为`1`)
- `create_fire` [可选][bool]爆炸是否创建火焰(默认为`false`)

## 坐标偏移
- `pos_src` [可选][int]位置来源 *默认为方块位置`0`, 玩家位置为`1`*
- `offset` [可选][Vec3d]偏移量 *默认为`(0.0, 0.0, 0.0)`*