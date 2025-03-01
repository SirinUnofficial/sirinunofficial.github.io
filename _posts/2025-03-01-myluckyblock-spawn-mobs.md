---
title: 7.生成生物
author: Sycamore0
date: 2025-03-01 23:17:00 +0800
categories: [简体中文, MyLuckyBlock]
tags: [MyLuckyBlock]
---

# 生成生物spawn_mobs

> 本条目基于MyLuckyBlock 1.2.0版本
{: .prompt-tip }

> 条目需要完善
{: .prompt-info }

## 基本
- `id` [string]生物id

## 坐标偏移
- `pos_src` [可选][int]位置来源 *默认为方块位置`0`, 玩家位置为`1`*
- `offset` [可选][Vec3d]偏移量 *默认为`(0.0, 0.0, 0.0)`*

## 生物名称
- `name` [可选][string]生物名称(默认为`null`)
- `name_visible` [可选][bool]生物名称是否始终可见 *默认为`false`*

## 生物年龄
- `is_baby` [可选][bool]生物是否为幼体 *默认为`false`*

## 生物数量
- `use_random` [可选][bool]是否使用随机数量 *默认为不使用, 即`false`*
- `random_num` [可选][Object]随机数量 *最大值默认为`1`, 最小值默认为`0`*
- `num` [可选][int]数量 *默认为`1`*
### 随机数量random_num
`use_random`为`true`时启用, 否则输入num。
 - `min` [int]最小数量 *默认为`0`*
 - `max` [int]最大数量 *默认为`1`*

## 速度
- `velocity` [可选][Vec3d]速度 *默认为`(0.0, 0.0, 0.0)`*

## NBT数据
- `nbt` [可选][string]NBT数据 *默认为`null`*