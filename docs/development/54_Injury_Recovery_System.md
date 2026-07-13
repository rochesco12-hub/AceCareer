# Ace Career Development Bible
# 54 · Injury Recovery System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Injury Recovery System 定义整个 Ace Career 的伤病与恢复系统。

伤病不是 RNG。真正导致伤病的是疲劳、年龄、赛程、恢复、训练、打法。因此伤病应该可以预测，也可以避免。很多传奇因为伤病提前结束，很多黑马因为恢复完成重新崛起。

---

# Design Goals

✓ 真实概率 ✓ 长期影响 ✓ Story Driven ✓ AI/玩家一致 ✓ Config Driven ✓ 不随机恶意惩罚 ✓ 百年稳定

---

# Nine Injury Categories

Minor / Muscle / Joint / Tendon / Stress / Illness / Chronic / Acute / Career Threatening

---

# Severity Levels

Very Minor → Minor → Moderate → Major → Severe → Career Threatening

---

# Risk Formula

```
Fatigue + Training Load + Match Load + Recovery + Age + Previous Injury = Risk
```

---

# Common Injuries

Ankle Sprain / Hamstring / Shoulder / Lower Back / Wrist / Elbow / Knee

---

# Recovery Process（五阶段）

```
Diagnosis → Treatment → Rehabilitation → Return → Match Fitness
```

- Medical Ready 85% → Match Ready 95% → Peak 100%（需要比赛找状态）
- Reinjury Risk：Recovery 90% → High Risk（刚复出再伤概率更高）

---

# Key Modifiers

- **Fatigue**：Fatigue 92 → Risk Very High（Today 自动提醒）
- **Training**：Extreme Training → Risk↑（长期累积）
- **Match Load**：10 Matches / 14 Days → Recovery↓ Risk↑
- **Recovery Quality**：Sleep + Recovery Training + Physio + Nutrition + Rest
- **Doctor Impact**：Elite Doctor → Recovery +15%
- **Physio Impact**：降低复发率，提高长期稳定性

---

# Career Impact

重大伤病永久影响：Movement↓ / Recovery↓ / Peak Window↓（不是恢复后就完全一样）

---

# Key Features

- **Chronic Injury**：Lower Back → Needs Management（不会完全消失）
- **Injury Story**：重大伤病自动触发 News→Story→Narrative→Comeback Arc
- **Injury Prevention**：主动 Recovery/Rest/Training Adjustment/Medical Team（伤病永远可管理）
- **Injury Report**：Today 展示 Current Risk/Recovery%/Expected Return/Medical Advice
- **AI Injury**：AI 完全遵循相同规则（传奇也可能因伤病陨落，新星可能因此崛起）

---

# Config Files

injury.json / recovery.json / injury_probability.json / medical.json

---

# Performance

- Risk Update <3ms
- Recovery Update <5ms
- 2200 Players Stable

---

# Definition of Done

✓ 真实伤病概率 ✓ AI/玩家一致 ✓ 完整恢复流程 ✓ Story 自动联动 ✓ Today 风险提示 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

职业生涯从来不是一条不断向上的曲线。真正的传奇不是从未受伤，而是在跌倒之后依然能够重新站起来。

Injury Recovery System 负责塑造职业生涯中最艰难也最动人的章节。

---

End of Document
