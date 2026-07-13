# Ace Career Development Bible
# 38 · Rivalry Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Rivalry Engine 定义整个 Ace Career 的宿敌系统。

职业网球最令人难忘的从来不是一个冠军，而是一段 Rivalry。Federer vs Nadal、Nadal vs Djokovic、Sampras vs Agassi——这些传奇不是由一次交手创造，而是由十几年共同书写。

---

# Design Goals

✓ 自动生成 ✓ 长期发展 ✓ Story Driven ✓ AI/玩家一致 ✓ Config Driven ✓ 百年稳定 ✓ 不依赖脚本

---

# Rivalry Lifecycle

```
First Meeting → Growing Rivalry → Classic Rivalry → Historic Rivalry → Final Meeting → Legacy
```

退役后依然存在。

---

# Rivalry 五级

Competitive → Emerging → Major → Classic → Historic（自动升级）

---

# Rivalry Trigger（需满足）

Matches ≥ 5 + Ranking Similar + Close Results + Major Tournaments → 才开始形成

---

# Rivalry Score

```
Meeting Frequency + Match Quality + Importance + Competitiveness + Story Weight = Rivalry Score
```

---

# 关键 Modifiers

- **Competitiveness**：15:14 >> 15:2（越接近越容易成为 Historic）
- **Tournament Weight**：Grand Slam Final ★5 / Masters Final ★4 / ATP250 ★2
- **Ranking Modifier**：No.1 vs No.2 → Weight +40%
- **Surface Rivalry**：Clay Rival / Grass Rival / Hard Rival（不同场地不同故事）
- **Era Modifier**：Peak Overlap 10 Years → Historic
- **Match Quality**：Five Sets / Tiebreak / Epic Comeback → 自动加分

---

# Key Features

- **Emotional Momentum**：Lost 5 Straight → Next Meeting Pressure↑
- **Signature Matches**：每段 Rivalry 自动挑选 Top10 经典之战
- **Rivalry Timeline**：2028 First Match→2030 First Final→2032 Grand Slam Final→2037 Last Match
- **AI Awareness**：Lost 6 → Train Harder / Skip Event / Target Revenge
- **Crowd Interest**：自动提高 Attendance/TV Rating/Media Coverage/Story Weight
- **Rivalry Ending**：Retirement/Different Tours → 进入 History
- **Historic Rivalries**：世界自动保存 Top Rivalries / All Time / Era

---

# Config Files

rivalry.json / head_to_head.json / importance.json / era.json

---

# Performance

- Rivalry Update <5ms
- H2H Query Realtime
- Timeline Build <10ms

---

# Definition of Done

✓ 自动生成宿敌 ✓ H2H 永久记录 ✓ Story 深度联动 ✓ AI 感知 Rival ✓ Timeline 自动生成 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

伟大的冠军定义一个时代。伟大的宿敌定义整个网球历史。

Rivalry Engine 负责创造那些多年以后仍然会被球迷反复讲述的经典对决。

---

End of Document
