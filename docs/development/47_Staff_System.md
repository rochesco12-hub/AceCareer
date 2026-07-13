# Ace Career Development Bible
# 47 · Staff System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Staff System 定义整个 Ace Career 的职业团队系统。

现代职业网球早已不是一个人的运动。Staff System 负责构建整个职业团队：教练、体能教练、理疗师、医生、营养师、数据分析师、经纪人。团队成员不直接增加能力值，而是影响成长速度/恢复效率/伤病风险/职业规划/收入/媒体曝光。

---

# Design Goals

✓ 长期成长 ✓ AI/玩家一致 ✓ Config Driven ✓ 职责明确 ✓ 不直接加能力 ✓ 团队经营 ✓ 百年稳定

---

# Seven Staff Roles

| Role | 职责 |
|------|------|
| Head Coach | Training / Career Planning / Tournament Schedule / Technique |
| Fitness Coach | Strength / Movement / Endurance / Conditioning（降低 Fatigue）|
| Physio | Recovery / Massage / Rehabilitation / Injury Prevention |
| Doctor | Diagnosis / Treatment / Surgery / Medical Advice |
| Nutritionist | Diet / Hydration / Body Composition / Recovery Nutrition |
| Analyst | Opponent Analysis / Surface Statistics / Match Reports / Shot Patterns |
| Agent | Sponsors / Media / Contracts / Appearance Fees（商业系统核心）|

---

# Staff Levels

Local → Professional → Elite → World Class

---

# Key Features

- **Staff Reputation**：Worked With 5 No.1 Players → Legendary Physio
- **Staff Relationship**（0~100）：合作越久效果越稳定
- **Team Synergy**：Elite Coach + Elite Physio → Recovery↑ Growth↑（整体>个体）
- **Staff Hiring**：Hire / Replace / Upgrade / Dismiss（AI 自动进行）
- **Staff Cost**：每周 Salary → Career Economy → Net Income（真实职业压力）
- **Staff Growth**：Young Physio→Experience→Elite Physio（世界持续演化）
- **Staff Retirement**：工作人员同样退休，新成员自动加入世界
- **AI Staff**：AI 根据 Money/Goals/Ranking/Age 自动调整团队，不会无限雇佣顶级成员
- **Staff Events**：New Agent / Coach Retirement / Medical Team Upgrade → Story
- **Media Connection**：Former No.1 Coach Joins Logan → News 自动报道
- **Economy Connection**：顶级团队 = 更高成本

---

# Config Files

staff.json / staff_levels.json / staff_salary.json / staff_roles.json

---

# Performance

- Staff Update <5ms
- Relationship Update Realtime
- Weekly Simulation <20ms

---

# Definition of Done

✓ 完整职业团队 ✓ AI 自动管理团队 ✓ 长期关系成长 ✓ Team Synergy ✓ Story 自动联动 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

职业网球从来不是一个人的胜利。每一座冠军奖杯的背后都站着一整个团队。

Staff System 负责让这些默默无闻的人真正成为职业生涯不可或缺的一部分。

---

End of Document
