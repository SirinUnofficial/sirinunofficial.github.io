---
title: 4.放置箱子
author: Sycamore0
date: 2025-03-01 23:14:00 +0800
categories: [简体中文, 我的幸运方块
tags: [我的幸运方块]
---

# 放置箱子place_chests

> 本条目基于MyLuckyBlock 1.2.0版本
{: .prompt-tip }

> 条目需要完善
{: .prompt-info }

## 基本
- `id` [string]战利品表id(默认为`empty`)

## 箱子类型
- `type` [可选][int]箱子类型(默认为`0`,即箱子)

## 坐标偏移
- `pos_src` [可选][int]位置来源 *默认为方块位置`0`, 玩家位置为`1`*
- `offset` [可选][Vec3d]偏移量 *默认为`(0.0, 0.0, 0.0)`*