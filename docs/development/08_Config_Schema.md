# Ace Career Development Bible
# 08 · Config Schema

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Config Schema 定义整个 Ace Career 的配置系统。

Config 是整个游戏唯一允许保存规则、参数、平衡、默认值的地方。

Engine 永远读取 Config。UI 永远读取 Engine。任何数值禁止写死在代码中。

---

# Design Goals

✓ 所有参数配置化 ✓ 热更新 ✓ 易于平衡 ✓ 易于扩展 ✓ 不影响存档 ✓ 支持未来 Mod

---

# Design Philosophy

错误：`let championPoints = 2000`

正确：`ranking_points.json` → Engine 只读取 Config

---

# Config Architecture（12 个模块）

```text
Config/
├── ranking/         积分规则（大满贯/Masters/ATP/Challenger/ITF各轮积分）
├── tournament/      赛事配置（签表规模/资格赛/种子/场地/赛制/球速）
├── growth/          成长曲线（年龄-成长率对照表）
├── training/        训练收益（各项训练成长值/疲劳增加/信心变化）
├── fatigue/         疲劳模型（比赛/旅行/训练各自疲劳值）
├── injury/          伤病模型（疲劳阈值/训练风险/比赛风险百分比）
├── recovery/        恢复配置（休息/理疗/按摩各自恢复值）
├── economy/         经济配置（教练薪资/医疗/旅行/酒店/赞助/通胀）
├── ai/              AI 配置（赛事偏好权重/恢复权重/风险偏好）
├── narrative/       叙事触发（连胜阈值/爆冷阈值/故事触发条件）
├── gameplay/        玩法默认值（自动保存/教程/难度/赛季长度）
└── system/          系统配置（数据库版本/存档版本/最低支持版本）
```

---

# Key Rules

- Config 按模块拆分为独立 JSON 文件，禁止一个巨大 JSON
- Config 永远不进入 Save；Save 只保存 Config Version
- 启动时 Config 全部进入内存缓存，Engine 只读缓存不重复读文件
- 开发模式支持 Hot Reload，无需重新编译调平衡
- 启动时自动验证（重复 ID / 无效范围 / 缺失字段 / 循环引用）

---

# Performance

- Config Load <20ms
- Validation <10ms
- Memory <5MB
- Hot Reload <50ms

---

# Future

✓ DLC ✓ Seasonal Balance ✓ Event Config ✓ WTA Config ✓ Online Config ✓ Experimental Config

---

# Definition of Done

✓ 所有数值配置化 ✓ Engine 无硬编码 ✓ 支持热更新 ✓ 版本管理 ✓ Save 与 Config 分离 ✓ 调平衡无需修改代码

---

# Final Principle

Engine 决定世界如何运行。Config 决定世界运行的规则。任何规则都不应该写进代码。

---

End of Document
