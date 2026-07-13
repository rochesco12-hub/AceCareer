# Ace Career Development Bible
# 57 · Retirement Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Retirement Engine 定义整个 Ace Career 的退役系统。

退役不是一个按钮，不是年龄到了自动消失，而是职业生涯最后一段最重要的旅程。所有 Career 最终都会来到这里。

---

# Design Goals

✓ 自然发生 ✓ AI/玩家一致 ✓ Story Driven ✓ Config Driven ✓ 告别赛季 ✓ Hall Of Fame ✓ 百年稳定

---

# Retirement Lifecycle

```
Peak → Decline → Considering Retirement → Farewell Season → Final Match → Retirement → Hall Of Fame
```

---

# Retirement Factors + Probability

```
Age + Decline + Injuries + Motivation = Retirement Chance（每周更新）
```

| Age Range | 描述 |
|-----------|------|
| 32~36 | Common |
| 37~40 | Veteran |
| 40+ | Rare |
| 28~31 | Early Retirement |

---

# Farewell Season（持续一个赛季）

- **Farewell Matches**：每站赛事自动标记"Last Appearance"（媒体/Story 自动引用）
- **Final Match**：对手/赛事/比分/日期永久记录 → Career Timeline 最后一页
- **Retirement Announcement**：自动生成 News→Media→Story→Timeline（世界级事件）

---

# 退役后流程

- **Ranking Freeze**：Ranking Archive→Removed→History（不继续参与世界排名）
- **Legacy Evaluation**：退役瞬间自动触发 Legacy Engine→Hall Evaluation→GOAT Ranking
- **Hall Of Fame**：满足条件自动进入 Hall（Retired→Hall Of Fame→Ceremony）
- **Career Documentary**：自动生成 Career Summary/Statistics/Highlights/Story Arc/Legacy

---

# Key Features

- **AI Retirement**：AI 同样拥有完整退役流程（传奇不断离开，新人不断出现）
- **Comeback**（Rare/未来）：Retired→Comeback→One More Season（概率极低）
- **Retirement Emotion**：传奇退役影响 Fans/Media/Rivals/World（整个赛季都在讨论）
- **Story Connection**：End Of An Era→Farewell Tour→Last Match→Legacy Begins
- **Today Integration**：Remaining Career Matches/Upcoming Farewell/Legacy Progress

---

# Config Files

retirement.json / farewell.json / hall.json / legacy_transition.json

---

# Performance

- Retirement Evaluation <5ms
- Hall Evaluation <10ms
- 2200 Players Stable

---

# Definition of Done

✓ AI 自然退役 ✓ Farewell Season ✓ Hall 自动评选 ✓ Story 深度联动 ✓ Career Documentary ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

职业生涯终究会结束。真正伟大的球员，离开的不是赛场，而是一个时代。

Retirement Engine 负责为每一位职业球员写下人生最后一章。

---

End of Document
