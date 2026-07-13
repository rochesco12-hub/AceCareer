# Ace Career Development Bible
# 30 · Tournament Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Tournament Engine 定义整个 Ace Career 的赛事运行系统。

它负责一项赛事从开始到结束的全部流程：报名→入围→种子→抽签→晋级→奖金→积分→冠军。真正的比赛由 Match Engine 完成。

---

# Design Goals

✓ 支持 ATP 全部赛事 ✓ Config Driven ✓ 自动运行 ✓ 未来 WTA ✓ 资格赛 ✓ 特殊赛事 ✓ 长期稳定

---

# Tournament Lifecycle

```
Created → Entry Open → Acceptance → Seeding → Draw → Round1→Round2→QF→SF→Final → Champion → Ranking → Archive
```

---

# 各阶段规则

| Phase | 内容 |
|-------|------|
| Entry | AI 自动决定 Enter/Skip/Withdraw（依据排名/疲劳/收益/场地/赛程）|
| Acceptance | Accepted / Qualifying / Alternate / Rejected（依据 Ranking/PR/Wildcard）|
| Seeding | 自动生成 Seed1~32（读取 Ranking Engine）|
| Draw | 32/64/96/128 签，种子分区+同国回避（可配置）+首轮轮空+Qualifier 填充 |
| Progression | R1→R2→R3→QF→SF→Final，每轮结束统一更新 |
| Walkover | 赛前退赛→Alternate 递补→不进入 Match Engine |
| Retirement | Match Engine 检测→Tournament 更新→冠军路线继续 |
| Lucky Loser | (未来) Qualifier 退赛→LL 进入 Main Draw |
| Prize | 赛事结束自动发放到 Player Finance/Career |
| Ranking | Champion → 积分统一更新到 Ranking Engine |
| Champion Ceremony | 自动生成 Story/News/Career Timeline/History |

---

# Tournament Importance

Grand Slam ★5 / Masters1000 ★4 / ATP500 ★3 / ATP250 ★2 / Challenger ★1 → 影响 Story/AI/News

---

# Key Features

- **Match Scheduling**（未来）：Centre Court/Court1/Court2 + 夜场/黄金时段
- **Weather Delay**（未来）：Rain→Schedule Delay→Next Day
- **Live Tournament**（未来）：Current Match/Current Round/Today's Schedule
- **Archive**：赛事结束自动保存 Champion/Draw/Results/Statistics/Prize/Ranking/Highlights/News → 永久 History
- **Story Hooks**：Upset/Young Champion/Title Defense/Historic Record/Five-set Epic 自动触发

---

# Config Files

tournament.json / draw.json / entry.json / prize.json / schedule.json

---

# Performance

- Draw Generation <20ms
- Tournament Progress <50ms
- Archive <20ms

---

# Definition of Done

✓ 自动报名 ✓ 自动抽签 ✓ 自动推进赛事 ✓ 自动发放积分奖金 ✓ 自动生成冠军 ✓ 自动进入历史 ✓ Config 驱动

---

# Final Principle

一项伟大的赛事不仅仅产生冠军。它还改变排名、创造传奇、书写历史。

Tournament Engine 负责让整个职业网球世界真正运转起来。

---

End of Document
