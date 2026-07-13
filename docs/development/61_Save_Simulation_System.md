# Ace Career Development Bible
# 61 · Save Simulation System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Save Simulation System 定义整个 Ace Career 的存档模拟系统。

存档不是保存一个画面，而是保存整个世界。玩家退出只是离开了这个世界，世界本身不会停止。

---

# Design Goals

✓ 世界持续运行 ✓ 存档安全 ✓ Config Driven ✓ AI/玩家一致 ✓ 百年稳定 ✓ 秒级加载 ✓ 可扩展

---

# Save Architecture

```
World State → Snapshot → Save File → Load → Resume Simulation
```

存档的是整个 World State，不是单独玩家。

---

# Save Contents

World / Players / Calendar / Ranking / Stories / History / Economy / Simulation State

---

# Key Features

- **Snapshot System**：Daily/Weekly/Season Snapshot（快速恢复）
- **Auto Save**：After Match/After Tournament/Weekly/Season End/Manual
- **Offline Simulation**：玩家离开后 AI Matches/Ranking/News/History 继续推进（速度可配置）
- **Simulation Speed**：Paused/Realtime/Fast/Very Fast
- **Deterministic**：Same Seed + Same World = Same Simulation（Debug/Replay 方便）
- **Save Integrity**：Atomic/Versioned/Recoverable（任何异常不损坏存档）
- **Save Migration**：v1→v2→v3 自动迁移（无需重新开档）
- **Multi Save**：Career A/B/C 完全独立互不影响
- **Cloud Sync**（未来）：iPhone→iPad→Mac 无缝同步
- **World Resume**：重新进入自动恢复 Calendar/Today/Simulation/Stories/Notifications

---

# Performance

- Save <100ms
- Load <300ms
- World Resume <500ms

---

# Definition of Done

✓ 自动存档 ✓ 自动恢复 ✓ 世界持续运行 ✓ 多存档支持 ✓ Version Migration ✓ Config 驱动

---

# Final Principle

玩家可以离开，世界不会暂停。真正活着的世界永远不会等待玩家。

---

End of Document
