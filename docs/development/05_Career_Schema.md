# Ace Career Development Bible
# 05 · Career Schema

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Career 是整个 Ace Career 中最重要的数据实体之一。

Player 描述的是"球员现在是谁"。Career 描述的是"球员这一生经历了什么"。

Career 永远不会被覆盖。只会不断增长。它代表的是一名职业球员完整的一生。

---

# Design Goals

✓ 永久保存职业生涯 ✓ 支持百年以上历史 ✓ 支持 Timeline

✓ Hall of Fame ✓ Story Engine ✓ Career Review ✓ 未来 Online Career

Career 永远采用 Append Only。绝不修改历史。

---

# Career Architecture（12 个模块）

```
Career
├── Identity         职业身份（PlayerID/起始赛季/结束赛季/状态）
├── Summary          职业概览（排名/冠军/奖金/胜场/负场）
├── Timeline         职业时间轴（Event 列表：首胜/首冠/Top100/大满贯/退役）
├── Rankings         排名历史（最高/最低/每周历史/年终/世界第一周数）
├── Titles           冠军记录（大满贯/Masters/ATP500/250/Challenger/ITF/奥运）
├── Records          职业纪录（最长连胜/最佳赛季/最多冠军/最快发球/胜率）
├── Rivalries        宿敌（对手/交手次数/胜负/宿敌等级）
├── Awards           奖项（年度最佳/进步最快/体育精神/奥运奖牌）
├── Statistics       职业统计（场地胜率/室内外/抢七/五盘/退赛）
├── Legacy           传奇数据（Legacy Score/GOAT排名/Hall of Fame分数）
├── Retirement       退役信息（赛季/年龄/原因/告别赛）
└── Metadata         系统信息
```

---

# Key Rules

- Career 与 Player **完全分离**：Player = 当前状态，Career = 完整历史
- Timeline 永远追加（Append Only），绝不删除
- Legacy Score 全部由 Engine 自动计算，禁止人工修改
- Career **不保存**：Current Fatigue / Coach / Tournament / Injury / Confidence（这些属于 Player）

---

# Career Milestones（自动记录）

首胜 / 首冠 / Top500 / Top100 / Top10 / 世界第一 / 大满贯 / 奥运冠军 / ATP Finals / 退役

---

# Archive Strategy

Career 永远保存。即使 Player 已退役也不删除。Hall Of Fame 直接引用 Career。

---

# Future Expansion

✓ Multiple Careers ✓ Online Career ✓ Hall Of Fame ✓ Story Replay ✓ Career Export ✓ Career Sharing

---

# Performance

- Career Query <10ms
- Timeline 支持 10000+ Events
- Career Lifetime 100 Years+

---

# Definition of Done

✓ Career 与 Player 完全分离 ✓ Timeline 永久追加

✓ 所有冠军引用 Tournament ✓ Legacy 自动计算

✓ Hall Of Fame 永久保存 ✓ 支持未来百年历史 ✓ Career 永不删除

---

# Final Principle

Player 描述的是今天。Career 记录的是一生。

当玩家多年以后重新打开这个存档，真正打动他的不是能力值，而是这一页完整的职业生涯。

---

End of Document
