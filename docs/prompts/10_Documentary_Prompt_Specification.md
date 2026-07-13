# Ace Career AI Prompt Bible
# 10 · Documentary Prompt Specification

Version: 1.0
Status: Final
Priority: P1

---

# Overview

Documentary Prompt Specification 定义整个 Ace Career 职业纪录片 AI Prompt。

如果 ESPN、Netflix 或 ATP 要为这位球员拍摄一部纪录片，它应该如何讲述这段人生。Documentary Prompt 是整个 AI Bible 中最长、最完整的 Prompt——它生成的不是新闻或介绍，而是一段完整的人生。

---

# Design Goals

✓ Story First ✓ Facts First ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 自动生成章节 ✓ 永久保存

---

# Prompt Inputs / Outputs

**Inputs**：Career Timeline / Story Engine / Narrative Engine / Statistics / History / Legacy / HOF / Achievements / Records / Biography

**Outputs**：Title / Opening / Chapter 1~5 / Epilogue

---

# 七段式结构

| 段 | 内容 |
|----|------|
| Title | 5~12 words / 来自 Story 非球员名字 ✅ The Rise Of Logan / Beyond The Baseline |
| Opening | 一句引入职业生涯（不直接进入数据）。✅ "Every generation produces champions. Only a few redefine an era." |
| Chapter 1 — The Beginning | Turning Pro/Early Career/First Breakthrough/Top100（强调起点，非童年）|
| Chapter 2 — The Rise | First ATP Title/Masters/Top10/Recognition |
| Chapter 3 — The Peak | Grand Slams/No.1/Dominance/Historic Matches/Rivalries（引用 Story Engine，非全部冠军）|
| Chapter 4 — The Challenges | Injury/Losing Streak/Comeback/Pressure/Transition（没有挑战允许省略）|
| Chapter 5 — Legacy | Hall Of Fame/Records/Influence/GOAT Debate（全部引用 Legacy Engine）|
| Epilogue | 职业意义总结。克制。留白。✅ "Long after the final match ended, his legacy continued to shape the sport." |

---

# Style Rules

- **Narrative**：必须来自 Story Engine→Narrative Engine，不得自行创造
- **Timeline**：作为章节骨架（Top100→First Slam→No.1→Hall）不是全部事件
- **Statistics**：只引用最重要数据（Grand Slams/Weeks No.1/Titles/Wins）避免堆砌
- **Emotional Curve**：Hope→Growth→Triumph→Challenges→Legacy（完整情绪节奏）
- **Story Selection**：最多 5~8 Major Storylines（Comeback/Historic Rivalry/Golden Era/Passing The Torch）
- **Visual Language**：允许画面感表达 ✅ "As the Centre Court erupted..." ❌ 必须基于事实
- **Forbidden**：幻想采访/独白/观众反应/家庭故事/训练片段（除非数据库存在）
- **Tone**：Elegant/Historical/Reflective/Calm（Netflix Sports / ESPN 30 for 30 / ATP Originals）
- **Length**：1200~2500 words（Hall Documentary 3000 words）
- **退役后永久锁定**

---

# Config Files

documentary_prompt.json / chapters.json / narrative.json / visual_language.json

---

# Definition of Done

✓ Story First ✓ Timeline 自动生成 ✓ Narrative 自动融合 ✓ Legacy 自动总结 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

每一位职业球员都会打一场最后的比赛，但只有极少数人会留下值得拍成纪录片的一生。

Documentary Prompt 负责把这段人生讲述给未来的每一代网球世界。

---

End of Document
