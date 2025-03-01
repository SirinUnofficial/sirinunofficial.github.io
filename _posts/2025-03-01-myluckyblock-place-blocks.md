---
title: 3.放置方块
author: Sycamore0
date: 2025-03-01 23:13:00 +0800
categories: [简体中文, MyLuckyBlock]
tags: [MyLuckyBlock]
---

# 放置方块place_blocks

> 本条目基于MyLuckyBlock 1.2.0版本
{: .prompt-tip }

## 基本
- `id` [string]方块id
### 在原地放置1个钻石块
```json
{
    "random_events": [
        {
            "id": 1,
            "place_blocks": [
                {
                    "id": "minecraft:diamond_block"
                }
            ]
        }
    ]
}
```

## 坐标偏移
- `pos_src` [可选][int]位置来源 *默认为方块位置`0`, 玩家位置为`1`*
- `offset` [可选][Vec3d]偏移量 *默认为`(0.0, 0.0, 0.0)`*
### 在玩家y+8的位置放置1个钻石块
```json
{
    "random_events": [
        {
            "id": 2,
            "place_blocks": [
                {
                    "id": "minecraft:diamond_block",
                    "pos_src": 1,
                    "offset": {
                        "x": 0,
                        "y": 8,
                        "z": 0
                    }
                }
            ]
        }
    ]
}
```
### 在y+4的位置放置一个钻石块, 并在原地也放一个
```json
{
    "random_events": [
        {
            "id": 4,
            "place_blocks": [
                {
                    "id": "minecraft:diamond_block",
                    "pos_src": 0,
                    "offset": {
                        "x": 0,
                        "y": 4,
                        "z": 0
                    }
                },
                {
                    "id": "minecraft:diamond_block"
                }
            ]
        }
    ]
}
```