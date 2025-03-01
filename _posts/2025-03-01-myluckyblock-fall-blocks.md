---
title: 5.掉落方块
author: Sycamore0
date: 2025-03-01 23:15:00 +0800
categories: [简体中文, MyLuckyBlock]
tags: [MyLuckyBlock]
---

# 掉落方块fall_blocks

> 本条目基于MyLuckyBlock 1.2.0版本
{: .prompt-tip }

> 条目需要完善
{: .prompt-info }

> 类似place_blocks
{: .prompt-info }
## 基本
- `id` [string]方块id

## 坐标偏移
- `pos_src` [可选][int]位置来源 *默认为方块位置`0`, 玩家位置为`1`*
- `offset` [可选][Vec3d]偏移量 *默认为`(0.0, 0.0, 0.0)`*