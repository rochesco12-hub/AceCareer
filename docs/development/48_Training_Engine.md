# Ace Career Development Bible
# 48 · Training Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Training Engine 定义整个 Ace Career 的训练系统。

训练不是点击按钮、不是经验值、不是每天固定加属性。Training Engine 是整个职业生涯成长的核心循环，连接 Growth/Fatigue/Recovery/Coach/Staff/Match/Career。训练不是升级，而是投资未来。

---

# Design Goals

✓ 长期成长 ✓ 数据驱动 ✓ Config Driven ✓ AI/玩家一致 ✓ 不可刷经验 ✓ 个性化训练 ✓ 百年稳定

---

# Eight Training Categories

| Category | 内容 | 特点 |
|----------|------|------|
| Technical | Serve/Forehand/Backhand/Volley/Return/Slice | 主要影响技术能力 |
| Physical | Strength/Speed/Acceleration/Endurance/Agility/Flexibility | Fatigue 更高 |
| Mental | Confidence/Focus/Pressure/Decision/Resilience | 成长慢但长期收益极高 |
| Tactical | Pattern Play/Court Position/Shot Selection/Opponent Analysis | 未来影响 Match Engine |
| Recovery | Stretch/Yoga/Mobility/Recovery Session | 不会提升能力但降低伤病风险 |
| Match Practice | Practice Set/Match Simulation/Tie-break Practice | 兼顾成长+比赛状态 |
| Surface | Clay Camp/Grass Preparation/Indoor Session | 提高对应场地表现 |
| Custom | 自由组合（Serve 40%+Movement 30%+Recovery 30%）| 个性化计划 |

---

# Training Intensity

Light → Normal → High → Extreme（强度越高成长越快，Fatigue 越高）

---

# Training Efficiency

```
Coach × Staff × Recovery × Confidence × Potential = Training Efficiency
```

---

# Key Features

- **Weekly Plan**：Mon Serve/Tue Fitness/Wed Recovery/Thu Match Practice/Fri Mental/Sat Recovery/Sun Rest（AI 同样执行）
- **Adaptive Training**：系统自动建议弱项训练方向（帮助而非强制）
- **Overtraining**：连续高强度 → Fatigue↑ Recovery↓ Injury↑ Growth↓（不存在无限训练）
- **Training Focus**：Attack/Defense/Movement/Consistency（未来影响打法形成）
- **Coach Influence**：Technical Coach→Serve↑ / Fitness Coach→Movement↑（不直接加属性）
- **Staff Influence**：Nutritionist→Recovery↑ / Physio→Injury↓（长期收益）
- **Training Reports**：每周生成 Improved/Fatigue/Focus/Recommendation → Today 直接展示
- **AI Training**：根据 Age/Weakness/Goals/Surface/Schedule 自动安排（形成不同成长路线）
- **Story Connection**：Serve Revolution / New Playing Style / Fitness Transformation

---

# Config Files

training.json / training_types.json / intensity.json / focus.json

---

# Performance

- Training Update <5ms
- Weekly Plan <10ms
- 2200 Players <40ms

---

# Definition of Done

✓ 多类型训练 ✓ AI 自动训练 ✓ 教练团队联动 ✓ Fatigue 深度参与 ✓ Story 自动生成 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

冠军不是在比赛中练出来的。冠军是在那些没有观众、没有掌声的训练日，一点一点塑造出来的。

Training Engine 决定每一位球员最终能够到达怎样的高度。

---

End of Document
