# Ace Career AI Prompt Bible
# 05 · Player Biography Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Player Biography Prompt Specification 定义整个 Ace Career 球员传记 AI Prompt。

Biography 不是个人简介，不是履历，而是一位球员留给世界的传记。读者读完应该知道：他是谁、为什么重要、他经历了什么、他给这个时代留下了什么。

---

# Design Goals

✓ Facts First ✓ Career First ✓ Story Driven ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 长期更新

---

# Prompt Inputs / Outputs

**Inputs**：Player Profile / Career / Timeline / Statistics / Story Tags / Achievements / Records / Legacy / Hall Of Fame / History

**Outputs**：Opening / Career Overview / Career Highlights / Playing Style / Legacy / Career Summary

---

# 六段式结构

| 段 | 内容 |
|----|------|
| Opening | 一句话定义球员。✅ "Logan Du is a professional tennis player whose career was defined by consistency..." ❌ 夸张/最高级 |
| Career Overview | Turning Pro/Career Length/Career High/Grand Slams/Titles/Wins（全部来自 Career）|
| Career Highlights | Timeline 自动引用：Top100→First Masters→First Slam→No.1→Hall Of Fame |
| Playing Style | 根据 Statistics 总结（Aggressive Baseliner/Strong Serve/Elite Return/Clay Specialist）不凭空描述 |
| Personality | 如果 Personality Engine 存在，引用 Calm/Professional/Resilient/Disciplined（不推测心理）|
| Legacy + Summary | Legacy Engine 引用 + 职业贡献总结（克制/类似 Wikipedia/ATP/Encyclopedia Britannica）|

---

# Style Rules

- **Story 融合**：Historic Comeback/Long Winning Streak/Great Rivalry（存在时自动融合，无则不生成）
- **Records**：必须 Records Engine 官方确认
- **Vocabulary**：✅ Established/Captured/Reached/Maintained/Developed/Recognized ❌ Greatest Ever/GOAT/Legendary（除非 Legacy Engine 已确认）
- **Forbidden**：梦想/童年故事/家庭背景/采访/心理活动/未来预测（除非数据库存在）
- **Length**：350~700 words（Hall Of Fame 1000 words）
- **Dynamic**：退役前持续更新，退役后锁定版本

---

# Config Files

biography_prompt.json / biography_style.json / career_structure.json / legacy_summary.json

---

# Definition of Done

✓ Facts First ✓ Career First ✓ Story 自动融合 ✓ Legacy 自动引用 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

真正优秀的人物传记不会告诉别人他赢了多少场比赛，而会告诉别人：为什么几十年以后这个世界依然记得他的名字。

---

End of Document
