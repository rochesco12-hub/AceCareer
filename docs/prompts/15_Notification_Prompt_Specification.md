# Ace Career AI Prompt Bible
# 15 · Notification Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Notification Prompt Specification 定义整个 Ace Career 所有通知的 AI Prompt。

Notification 是整个 Career 中最容易被滥用的 AI 内容。真正优秀的通知应该做到：不重要的事情不打扰，真正重要的事情一句话就够。"为什么现在必须告诉玩家"——如果不能回答，就不应该推送。

---

# Design Goals

✓ Importance First ✓ Action Driven ✓ Facts First ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 极短阅读时间

---

# Prompt Inputs / Outputs

**Inputs**：Calendar / Today / Match Result / Tournament / Ranking / Story Tags / Achievements / Injury / Training / Recovery / Notification Queue

**Outputs**：Title / Subtitle / Type / Priority / Deep Link（所有通知必须可点击）

---

# 11 Notification Categories

Match / Tournament / Ranking / Training / Recovery / Story / Achievement / Injury / Calendar / Reminder / World News

---

# Priority Levels

Critical（Grand Slam Final）/ High（World No.1）/ Medium / Low（Recovery Complete）/ Silent（Training Complete）

---

# 各类通知示例

| Category | Title | Subtitle |
|----------|-------|----------|
| Match | Quarterfinal Starts Today | Your match begins in two hours. |
| Result | Champion! | You captured your first Masters title. |
| Ranking | Career High Ranking | You move up to World No.12. |
| Achievement | 100 Career Wins | —（只推送重大成就）|
| Story | Winning Streak Reaches 10 | —（必须 High Priority 才推送）|
| Injury | Recovery Complete | —（保持专业）|
| Reminder | Tournament Tomorrow | —（来自 Calendar）|
| World | New World No.1 | Historic Retirement（只有重大事件）|

---

# Key Rules

- **Frequency**：每天最多 3 Push Notifications（Today 不限，Push 必须克制）
- **Duplicate**：禁止连续推送同类通知，系统自动合并
- **Deep Links**：Match→Match Detail / Ranking→Ranking Page / Story→Story Detail（禁止无入口）
- **Smart Timing**：考虑 Sleep/Timezone/Current Match/Calendar（凌晨不推送普通新闻）
- **同一事件只允许一次 Push**，后续更新 Today 不重复提醒
- **Vocabulary**：✅ Ready/Available/Champion/Improved/Reached/Completed ❌ Urgent/Amazing/Crazy/Epic/Breaking
- **Length**：Title 18~35 chars / Subtitle 30~60 chars（Apple HIG 优先）

---

# Config Files

notification_prompt.json / priority_rules.json / notification_types.json / deep_links.json

---

# Definition of Done

✓ Importance First ✓ Push 数量受控 ✓ Story 自动融合 ✓ Deep Link 完整 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

真正优秀的通知不会让玩家觉得"又来了一条推送"，而会让玩家觉得"这件事我现在就想打开看看"。

Notification Prompt 负责让每一次打扰都真正值得。

---

End of Document
