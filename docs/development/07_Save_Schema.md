# Ace Career Development Bible
# 07 · Save Schema

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Save Schema 定义整个 Ace Career 的存档系统。

它不是数据库，也不是 CloudKit。而是 **玩家职业生涯的完整快照（Snapshot）。**

Save 保存世界当前状态，保证玩家任何时候退出再进入，整个世界保持完全一致。

---

# Design Goals

✓ 自动保存 ✓ 秒级读取 ✓ 支持多个 Career ✓ Cloud Sync ✓ 版本迁移 ✓ Replay ✓ World Snapshot

---

# Design Philosophy

Save 不是 Database。Database 保存世界。Save 保存世界在某一个时间点的状态。Save 永远引用 Database，而不是复制整个世界。

---

# Save Architecture（10 个模块）

```
Save
├── Identity         存档身份（SaveID/CareerID/PlayerID/WorldID/最后游玩时间）
├── WorldState       世界状态（赛季/周次/赛历/当前赛事/World Seed）
├── PlayerState      玩家当前状态（当前赛事/疲劳/伤病/信心/位置/教练）
├── CareerState      职业状态（当前排名/职业状态/当前目标/Hall of Fame进度）
├── SimulationState  模拟状态（最后模拟周/待处理模拟/活跃故事/计划事件）
├── Settings         玩家设置（难度/语言/单位/通知/图形/辅助功能）
├── Statistics       游玩统计（游戏时间/会话数/自动保存次数）
├── Snapshot         存档缩略图（排名/赛季/周次/最近赛事/头条）
├── Version          版本控制（数据库版本/Engine版本/存档版本/迁移标记）
└── Metadata         系统信息（设备ID/Cloud状态/Checksum）
```

---

# Save Lifecycle

Create Career → Generate World → Create Save → Autosave → Cloud Sync → Load → Continue → Archive → Delete

---

# Autosave 触发时机

比赛结束 / 训练结束 / 恢复结束 / 推进 Week / 排名更新 / 获得冠军 / 退出游戏 / App 进入后台

---

# Key Rules

- Save **不保存**：Config / Algorithms / AI Logic / Ranking Rules / Tournament Templates（来自 Engine）
- 每个 Career 一个主存档 + 多个 Snapshot
- Save 只保存变化数据，默认压缩

---

# Cloud Sync

同步 Save（不是整个 Database）。冲突采用最新版本。未来支持 Merge。

---

# Performance

- Load Save <100ms
- Autosave <50ms
- Single Career <1MB
- 100 Careers <100MB

---

# Future

✓ Cross Device ✓ iCloud ✓ Steam Cloud ✓ Shared Career ✓ Replay ✓ Timeline Export

---

# Definition of Done

✓ Save 独立于 Database ✓ 自动保存 ✓ 支持无限 Career ✓ Cloud Sync

✓ 版本迁移 ✓ Snapshot ✓ 秒级恢复游戏

---

# Final Principle

玩家保存的不是一个文件。玩家保存的是一个仍然持续运转的职业网球世界。

每一次存档，都是这段职业生涯在时间长河中的一个坐标。

---

End of Document
