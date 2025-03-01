---
title: 1.添加事件
author: Sycamore0
date: 2025-03-01 23:11:00 +0800
categories: [简体中文, 我的幸运方块
tags: [我的幸运方块]
---

# 添加事件

> 本条目基于MyLuckyBlock 1.2.0版本
{: .prompt-tip }

# 简介
当前版本的MyLuckyBlock使用数据包的方式加载事件, 因此你需要创建一个数据包来添加新的事件。<br>
# 数据包结构
```
└─data
   └─myluckyblock
        ├─lucky_events
        │   ├─myluckyblock
        │   │     └─{新建事件id}.json
        │   │
        │   └─{新建幸运方块id}
        │         └─{新建事件id}.json
        │
        └─structure                    # 结构文件
```

# Json
## 头部
```json
{
    "name": "tutorial", // 名称
    "version": "1.0.0", // 版本号
    "info": "tutorial events", // 信息
    "random_events": [] // 随机事件
}
```
 - `name` [string]文件名
 - `version` [string]版本号
 - `info` [string]信息
 - `random_events` [Object]随机事件
## 随机事件randomEvents
### 目前开放的功能
- `drop_items` 掉落物品
- `place_blocks` 放置方块
- `fall_blocks` 掉落方块
- `create_explosions` 创建爆炸
- `spawn_mobs` 生成生物
- `give_potion_effects` 给予药水效果
- `send_messages` 发送消息
- `add_particles` 生成粒子
- `load_structures` 加载结构
- `execute_commands` 执行命令

## 特殊
### 位置来源pos_src
默认为`0`
 - `0` 方块
 - `1` 玩家
### 偏移量offset
默认为`{ x: 0, y: 0, z: 0 }`
 - `x` [float]x轴偏移量(默认为`0`)
 - `y` [float]y轴偏移量(默认为`0`)
 - `z` [float]z轴偏移量(默认为`0`)
### NBT数据
默认为`null`, 例如
```
"nbt": "{Glowing:1b,HandItems:[{id:\"minecraft:tnt\",Count:12b},{}],ArmorItems:[{},{},{},{id:\"minecraft:tnt\",Count:12b}]}"
```