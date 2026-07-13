# Ace Career Development Bible
# 19 · Balance System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Balance System 定义整个 Ace Career 的数值平衡体系。

它负责：**保证整个职业世界长期运行依然合理。** 即使连续模拟 100 个赛季，世界依然稳定。

---

# Design Goals

✓ 长期稳定 ✓ 完全配置化 ✓ 数据驱动 ✓ 易于调参 ✓ 支持 Simulation ✓ 支持 AI ✓ 支持 DLC

---

# Ten Core Balance Areas

```
Player Growth → Player Decline → Fatigue → Recovery → Injury
→ Tournament → Economy → Ranking → AI → World Population
```

---

# Key Balance Curves

**Growth**：16-18 ★5 / 19-21 ★4 / 22-25 ★3 / 26-29 ★2 / 30-32 ★1 / 33+ Decline

**Peak**：24~29（成长≈衰退的平衡期）

**Decline**：30(-0.2%) → 31(-0.4%) → 33(-0.9%) → 36(-1.8%) 平滑下降

**Injury**：全年轻伤 2~5 次，重伤极少。不是惩罚系统

**Economy**：Top10 极高收入 → Top100 稳定 → Top300 勉强盈利 → 500+ 可能亏损

**Ranking**：Top10 变化慢 / Top100 持续竞争 / Top500 流动最快

**Population**：Active 2200 / Junior 400，任何赛季保持稳定

---

# Balance Workflow

```
Collect Data → Simulation → Analyze → Adjust Config → Run Again → Compare → Ship
```

永远修改 Config，不是修改 Engine。

---

# Simulation Validation（每 10 年自动检查）

Average Ranking / Average Titles / Average Retirement Age / Population / Prize Inflation / World Strength

---

# KPI Targets（100 年模拟）

- Population Stable ✓
- Ranking Stable ✓
- Economy Stable ✓
- Career Length 15±3 Years
- Grand Slam Diversity ✓

---

# Balance Sheets

Growth.xlsx / Fatigue.xlsx / Recovery.xlsx / Ranking.xlsx / Economy.xlsx / AI.xlsx / Tournament.xlsx / Population.xlsx

Engine 永远读取这些配置。

---

# Definition of Done

✓ 数值长期稳定 ✓ 全部配置化 ✓ 支持 100 年模拟 ✓ AI 行为合理 ✓ 排名稳定流动 ✓ 世界人口稳定 ✓ 经济系统稳定

---

# Final Principle

真正优秀的平衡不是玩家感觉不到，而是玩家永远觉得：这个职业网球世界，本来就应该这样运行。

---

End of Document
