---
title: 2.掉落物品
author: Sycamore0
date: 2025-03-01 23:10:00 +0800
categories: [简体中文, MyLuckyBlock]
tags: [MyLuckyBlock]
---

# 掉落物品drop_items

> 本条目基于MyLuckyBlock 1.2.0版本
{: .prompt-tip }

## 基本
- `id` [string]物品id
- `use_random` [可选][bool]是否使用随机数量 *默认为不使用, 即`false`*
- `random_num` [可选][Object]随机数量 *最大值默认为`1`, 最小值默认为`0`*
- `num` [可选][int]数量 *默认为`1`*
### 随机数量random_num
`use_random`为`true`时启用, 否则输入num。
 - `min` [int]最小数量 *默认为`0`*
 - `max` [int]最大数量 *默认为`1`*
### 在原地掉落5个钻石
```json
{
    "random_events": [
        {
            "id": 1,
            "drop_items": [
                {
                    "id": "minecraft:diamond",
                    "num": 5
                }
            ]
        }
    ]
}
```
### 在原地掉落1~10个钻石
```json
{
    "random_events": [
        {
            "id": 2,
            "drop_items": [
                {
                    "id": "minecraft:diamond",
                    "use_random": true,
                    "random_num": {
                        "max": 10,
                        "min": 1
                    },
                    "pos_src": 0
                }
            ]
        }
    ]
}
```

## 坐标偏移
- `pos_src` [可选][int]位置来源 *默认为方块位置`0`, 玩家位置为`1`*
- `offset` [可选][Vec3d]偏移量 *默认为`(0.0, 0.0, 0.0)`*
### 在玩家y+8的位置掉落1个钻石, 并在原地掉落2个tnt
```json
{
    "random_events": [
        {
            "id": 3,
            "drop_items": [
                {
                    "id": "minecraft:diamond",
                    "pos_src": 1,
                    "offset": {
                        "x": 0,
                        "y": 8,
                        "z": 0
                    }
                },
                {
                    "id": "minecraft:tnt",
                    "num": 2,
                    "pos_src": 0
                }
            ]
        }
    ]
}
```

## NBT数据
> v1.2.1新增特性
{: .prompt-info }

- `nbt` [可选][string]nbt数据 *默认为`null`*
### 在原地掉落1个带NBT的钻石
但是带有nbt[rarity=rare,enchantments={levels:{vanishing_curse:1}}]
```json
{
    "random_events": [
        {
            "id": 4,
            "drop_items": [
                {
                    "id": "minecraft:diamond",
                    "num": 1,
                    "nbt": "rarity=rare,enchantments={levels:{vanishing_curse:1}}"
                }
            ]
        }
    ]
}
```