# Ace Career AI Prompt Bible
# 16 · Achievement Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Achievement Prompt Specification 定义整个 Ace Career 成就系统 AI Prompt。

Achievement 不只是一个 Badge——它代表职业生涯的重要里程碑。每一个 Achievement 都应该成为 Career Timeline 的一个节点、History Archive 的一部分、Story Engine 的素材。Achievement 不是奖励，而是历史节点。

---

# Design Goals

✓ Milestone First ✓ Facts First ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 庄重但克制 ✓ 永久可回顾

---

# Prompt Inputs / Outputs

**Inputs**：Achievement / Career / Timeline / Statistics / Story Tags / Records / Ranking / Tournament / Legacy

**Outputs**：Achievement Title / Milestone / Description / Historical Context / Next Goal

---

# 8 种 Achievement Categories

| Category | 示例 |
|----------|------|
| Career | Professional Debut / First ATP Win / 100 Matches / 500 Wins / Retirement |
| Ranking | Top100 / Top50 / Top10 / World No.1 / Year-end No.1 |
| Tournament | First ATP Title / Masters Champion / Grand Slam / Career Slam / Olympic Gold |
| Statistics | 1000 Aces / 10000 Games Won / 80% Win Rate / 500 Tie-break Wins |
| Story | Comeback Complete / 10 Match Streak / Underdog Champion / Historic Rivalry |
| Records | Longest Streak / Most Masters / Youngest Champion（Records Engine 确认）|
| Legacy | Hall Of Fame / GOAT Top10 / Legend Tier / Immortal Tier |
| Special | 特殊事件成就 |

---

# 五段式结构

| 段 | 内容 |
|----|------|
| Title | 5~10 words |
| Milestone | 成就等级（Bronze/Silver/Gold/Legend/Immortal）不是稀有度而是职业意义 |
| Description | 一句话解释为什么重要 ✅ "You entered the Top 10 for the first time in your career." |
| Historical Context | 历史背景 ✅ "Only the fifth player from your country to reach World No.1."（必须 History Engine 支持）|
| Next Goal | 自动推荐下一目标 ✅ "Next: Win Your First Grand Slam"（来自 Career Goal Engine）|

---

# Style Rules

- **Tone**：Proud/Professional/Respectful/Calm（不是游戏奖励）
- **Vocabulary**：✅ Reached/Achieved/Completed/Captured/Established ❌ Unlocked!/Level Up!/Mission Complete!/Epic Reward!
- **Forbidden**：幻想未来/采访/奖励/游戏术语/经验值/金币

---

# Config Files

achievement_prompt.json / achievement_levels.json / milestones.json / next_goals.json

---

# Definition of Done

✓ Milestone First ✓ Facts First ✓ Timeline 自动记录 ✓ History 自动归档 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

真正值得纪念的从来不是获得一个徽章，而是在人生的某一天你真正跨过了一个新的高度。

Achievement Prompt 负责让每一个里程碑都成为职业生涯不可替代的一页。

---

End of Document
