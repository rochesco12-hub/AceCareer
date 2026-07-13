# Ace Career Game Design Document
## Product Roadmap & Development Milestones

Version: 1.0
Status: Final
Priority: P0

---

# 1. Purpose

Roadmap 定义 Ace Career 从 Alpha 到正式版的完整开发路线。

它不是功能列表。

而是整个项目的开发顺序。

开发原则：

**先建立世界（World），再建立玩法（Gameplay），最后增加内容（Content）。**

绝不能反过来。

---

# 2. Development Philosophy

整个项目遵循四个原则：

### Rule 1

先完成底层系统。

不要急着做 UI。

没有稳定的数据结构。

任何 UI 都会推倒重来。

---

### Rule 2

所有系统必须互相独立。

例如：

Ranking 不依赖 UI。

Training 不依赖 Match。

News 不依赖 Today。

全部通过 Event 通信。

---

### Rule 3

所有系统必须支持长期 Career。

不是：

打一站比赛。

而是：

连续模拟 30~50 个赛季。

---

### Rule 4

任何功能上线之前。

必须能够通过：

World Simulation。

---

# 3. Phase 1 — Core Engine

目标：

建立整个职业网球世界。

必须完成：

- Calendar
- Tournament
- Entry
- Acceptance
- Draw
- Match Week
- Ranking
- Save
- State Machine
- Data Model

完成标准：

能够连续模拟：

10 个赛季。

不会崩。

---

# 4. Phase 2 — Career Gameplay

目标：

玩家真正可以开始职业生涯。

新增：

- Today
- Training
- Injury
- Recovery
- Coach
- Finance
- Match Simulation
- Progression

完成标准：

玩家可以：

从 ITF 打到 ATP。

---

# 5. Phase 3 — Living World

目标：

世界真正活起来。

新增：

- News
- AI Career
- Rookie
- Retirement
- Hall of Fame
- Legacy
- Rival
- Records

完成标准：

玩家感觉：

世界不依赖自己。

---

# 6. Phase 4 — Content Expansion

新增：

- 更多赛事
- 更多国家
- 更多球员
- 更多装备
- 更多教练
- 更多赞助商

核心系统：

不修改。

只增加内容。

---

# 7. Phase 5 — Polish

优化：

动画。

音效。

UI。

交互。

性能。

AI。

平衡。

所有数值。

全部微调。

---

# 8. MVP

第一个可玩的版本：

包含：

✓ 创建 Career

✓ Week Mode

✓ Tournament Entry

✓ Match Simulation

✓ Ranking

✓ Training

✓ Injury

✓ Save

✓ AI Career

✓ News

✓ Retirement

玩家：

可以完整经历：

一位职业球员的一生。

---

# 9. Alpha

目标：

证明：

Career Loop。

流程：

```text
Create Career
↓
Train
↓
Enter Tournament
↓
Play Match
↓
Gain Points
↓
Ranking
↓
Next Week
```

所有流程：

跑通。

---

# 10. Beta

新增：

完整世界。

包括：

- Hall Of Fame
- Rival
- Legacy
- Rookie
- Coach Team
- Sponsor
- Economy

世界：

真正拥有历史。

---

# 11. Version 1.0

正式版：

完成：

全部核心系统。

支持：

50+ Season。

AI：

完整职业生涯。

世界：

持续演化。

---

# 12. Version 2.0（Future）

新增：

- ATP Finals
- Davis Cup
- Olympics
- UTS
- Laver Cup
- Doubles Career
- Mixed Doubles
- Junior Career
- Women's Tour（WTA）

---

# 13. Version 3.0（Future）

新增：

Online Universe。

多个玩家：

共享：

同一个职业世界。

包括：

- Online Career
- Transfer Market
- Online Rival
- Global Ranking
- Weekly Events

---

# 14. Technical Milestones

Engine：

完成。

↓

World：

完成。

↓

Gameplay：

完成。

↓

AI：

完成。

↓

Balance：

完成。

↓

Content：

完成。

↓

Release。

---

# 15. Success Metrics

项目达到以下标准：

✓ 连续模拟 50 个赛季

✓ 世界不会停止

✓ AI 正常成长

✓ 新秀正常生成

✓ 排名稳定

✓ 新闻持续更新

✓ 玩家职业生涯完整

✓ Save 永不损坏

✓ 世界历史永久保存

---

# 16. Final Vision

Ace Career 最终目标不是：

做一个网球游戏。

而是：

建立一个真正会不断发展的职业网球世界。

玩家不是唯一主角。

世界不会等待玩家。

传奇会退役。

新秀会崛起。

纪录会被打破。

历史会不断书写。

每一次 Career。

都会拥有完全不同的故事。

---

# Definition of Done

当玩家完成 30 年职业生涯后。

回顾 Career Timeline。

能够清楚记住：

- 自己的成长。
- 伟大的对手。
- 伟大的比赛。
- 伟大的冠军。
- 伟大的时代。

这就是 Ace Career 成功的标准。

---

End of Document
