# Ace Career Development Bible
# 06 · World Schema

Version: 1.0
Status: Final
Priority: P0

---

# Overview

World 是整个 Ace Career 唯一的 Root Object（根对象）。

所有数据最终都属于 World。如果把 Player 删除，世界依然存在。如果删除 World，整个 Career 就不存在。

---

# Design Goals

✓ 整个职业世界只有一个 Root ✓ 世界可以独立运行 ✓ 支持无限赛季

✓ 未来 Online World ✓ 多人共享世界 ✓ 世界快照 ✓ DLC 与扩展

---

# World Architecture（12 个模块）

```
World
├── Identity         世界身份（WorldID/Seed/当前赛季/当前周/版本）
├── Calendar         世界赛历（赛季/周次/当前赛事/下一站/休赛期）
├── Population       世界人口统计（活跃/青少年/退役/名人堂/新增/退役数）
├── Rankings         世界排名（ATP/Race/年终/历史第一/排名历史）
├── Tournaments      赛事集合（活跃/即将/已完成/历史归档）
├── News             世界新闻（最新/精选/突发/历史）
├── History          世界历史（冠军/纪录/Hall of Fame/时间轴）
├── Seasons          赛季状态（当前/已完成/赛季历史/休赛期）
├── Economy          世界经济（通胀/奖金池/赞助市场/旅行成本/教练市场）
├── Environment      世界环境（天气种子/场地速度/球类型/场地条件）
├── Simulation       模拟状态（模拟周/最后模拟/世界状态/待处理事件）
└── Metadata         系统信息
```

---

# World Population（默认）

Active Players: 2200 | Junior: 400 | Hall Of Fame: Unlimited | Retired: Unlimited

World 永远维护人口平衡。

---

# Key Rules

- World 是唯一 Root，所有对象最终都属于 World
- World Seed 决定整个世界，同一 Seed 生成同一世界
- World **不保存**：Player Attributes / Match Score / Coach Details / Training Data（属于各自 Schema）
- Rankings 完整榜单属于 World，Player 只保存自己的 Current Ranking

---

# Read/Write Flow

- **启动**：World → Season → Calendar → Current Week → Player → Today
- **推进一周**：World Simulation → Tournament → Ranking → News → History → World → Save

---

# Future

✓ World Snapshot（Replay/Debug/Cloud Recovery）✓ ATP/WTA/Junior/Doubles/Davis Cup/Olympics/Online Shared World

---

# Performance

- World Load <20ms
- Week Advance <100ms
- 100 Seasons Supported
- World Size <250MB

---

# Definition of Done

✓ World 成为唯一 Root Object ✓ 世界状态唯一 ✓ 排名统一管理

✓ Calendar 唯一管理 ✓ History 永久保存 ✓ 支持无限赛季 ✓ 支持未来多人世界

---

# Final Principle

Ace Career 的主角不是玩家，而是整个职业网球世界。

Player 会退役。冠军会更替。纪录会被打破。但 World 将一直存在。

---

End of Document
