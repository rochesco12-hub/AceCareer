# Ace Career AI Prompt Bible
# 03 · Match Report Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Match Report Prompt Specification 定义整个 Ace Career 比赛战报的 AI Prompt。

News 偏向新闻。Match Report 更偏向比赛分析。它将永久保存在 Match Page、Tournament Archive、Career Timeline、Replay、History。多年以后玩家再次打开这场比赛，仍然能知道这场比赛为什么重要。

---

# Design Goals

✓ Facts First ✓ Match First ✓ Story Driven ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 永久可读

---

# Prompt Inputs / Outputs

**Inputs**：Match / Tournament / Surface / Round / Players / Statistics / Momentum / Story Tags / Timeline / Ranking / Records

**Outputs**：Headline / Summary / Turning Point / Statistics / Impact / Next Step

---

# 六段式结构

| 段 | 内容 |
|----|------|
| Headline | 8~16 words / 描述结果 / 不制造悬念 ✅ Logan Claims First Wimbledon Crown |
| Summary | Who Beat Who + Score + Tournament + Round |
| Match Flow | Opening Set→Momentum Shift→Final Set→Closing Moments（比赛过程而非数据堆积）|
| Turning Point | 真正改变比赛的瞬间（引用 Story Engine，不得幻想）|
| Statistics | 3~6 项关键数据（Ace/DF/1st Serve%/Break Points/Winners/UE/Duration）不全部罗列 |
| Impact + Next | Ranking/Titles/Story/Legacy/Records + Next Opponent/Upcoming Final |

---

# Style Rules

- **Vocabulary**：✅ Controlled/Recovered/Shifted/Dominated/Held Firm ❌ Crushed/Destroyed/Annihilated
- **Emotion**：✅ Composed/Confident/Resilient/Patient ❌ Miracle/Impossible/Godlike/Unbelievable
- **Length**：180~350 words（重要比赛 500 words）
- **Player Perspective**：禁止猜测心理。❌ "他一定非常激动" ✅ "这是他职业生涯首座大满贯冠军"
- **Forbidden**：采访/内心活动/观众对话/教练讲话/社交媒体/未来预测
- **Statistics Priority**：Score→Momentum→Serve→Return→Pressure Points（不是随机）
- **Story Tags**：存在时自然融入（Comeback/Revenge/Underdog/Historic Rivalry），没有不得创造

---

# Config Files

match_report_prompt.json / report_structure.json / vocabulary.json / length_rules.json

---

# Definition of Done

✓ Match First ✓ Facts First ✓ Story Driven ✓ Statistics Accurate ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

真正优秀的比赛战报不是告诉读者比分，而是告诉读者：为什么这场比赛值得多年以后再次阅读。

---

End of Document
