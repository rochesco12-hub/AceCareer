# Ace Career Development Bible
# 04 · Match Schema

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Match 是 Ace Career 中最小的正式比赛单位。

整个 Tournament 由多个 Match 组成。整个 Career 由数千场 Match 组成。

Match Schema 不负责模拟比赛。Match Engine 负责计算。Match Schema 负责记录。

---

# Design Goals

✓ 完整记录每一场比赛 ✓ 支持所有赛事 ✓ 未来双打

✓ 实时比赛 ✓ 完整统计 ✓ 回放 ✓ 历史永久保存

---

# Match Architecture（12 个模块）

```
Match
├── Identity         比赛身份（赛事/轮次/球场/编号）
├── Participants     参赛双方（PlayerID/种子/排名快照）
├── Schedule         时间安排（开始/结束/时长/时区）
├── Rules            赛制快照（三盘/五盘/抢七/Super Tie-break）
├── Score            比分（盘分/局分/抢七/退赛/Walkover）
├── Statistics       技术统计（Ace/双误/一发得分率/破发点/Winner/UE/网前）
├── Momentum         比赛走势（时间线/转折点/最大领先/逆转时刻）
├── Events           比赛事件（医疗暂停/挑战/雨停/伤退/警告）
├── Result           比赛结果（胜者/积分/奖金/完成原因）
├── Status           比赛状态（Scheduled/Warmup/Live/Suspended/Finished/Archived）
├── Highlights       精彩时刻（最佳一分/转折点/故事标签/AI摘要）
└── Metadata         系统信息
```

---

# Match Lifecycle

Created → Scheduled → Warmup → Live → Finished → Statistics → Archive

---

# Key Rules

- Match **不保存**：Player Attributes / Ranking / Career / Coach / Training / Recovery
- 所有外部对象以 ID 引用
- 比赛结束后自动进入 Archive，永久保存

---

# Future: Live Match

```swift
LiveState {
    currentServer / currentGameScore / currentPoint / liveMomentum / elapsedTime
}
```

不影响历史结构。

---

# Future: Replay

读取 Events → Momentum → Highlights → Score Timeline，无需重新模拟。

---

# Performance

- Match Query <5ms
- Statistics Query <10ms
- Replay Load <30ms
- History 永久保存

---

# Definition of Done

✓ Match 拆分为 12 个模块 ✓ Score 与 Statistics 分离

✓ 支持实时比赛 ✓ 支持历史回放 ✓ 支持未来双打

✓ 支持 AI Story Engine ✓ 永久保存比赛历史

---

# Final Principle

一场比赛不仅决定胜负。

它还会改变排名、创造新闻、诞生纪录、塑造宿敌，最终成为整个职业生涯历史的一部分。

---

End of Document
