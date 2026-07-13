# Ace Career Development Bible
# 40 · Achievement System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Achievement System 定义整个 Ace Career 的成就系统。

Achievement 不是任务系统，更不是签到奖励。Achievement 是职业生涯的重要纪念，它让玩家意识到自己已经走了多远。

---

# Design Goals

✓ 自然获得 ✓ Story 驱动 ✓ 长期目标 ✓ AI/玩家一致（部分）✓ Config Driven ✓ 隐藏成就 ✓ 百年稳定

---

# 12 种 Achievement Categories

| Category | 示例 |
|----------|------|
| Career | Professional Debut / First ATP Win / 100 Matches / 500 Matches / Retirement |
| Tournament | First ATP250 / First Masters / First Grand Slam / Career Slam / Golden Slam |
| Ranking | Top500 / Top100 / Top50 / Top10 / No.1 / 100 Weeks No.1 |
| Records | Fastest Serve / Longest Streak / Most Aces / Historic Record |
| Rivalry | First Rival / 10 Meetings / Win Historic Rivalry / Grand Slam Revenge |
| Statistics | 1000 Aces / 500 Winners / 90% Win Rate / 100 Match Points Saved |
| Collection | Win All Slams / All Masters / All Surfaces / All Continents |
| Challenge | Win Without Losing A Set / Win From Two Sets Down / Win 20 Matches Straight |
| Historic | Youngest No.1 / Oldest Champion / Calendar Slam / Golden Career |
| Legacy | Hall Of Fame / GOAT Candidate / All-time Great（退役后自动获得）|
| Hidden | Win Match After Injury / Beat No.1 As Qualifier / Three Comebacks In One Season |
| Season | 50 Wins / 3 Titles / Year-end No.1 / ATP Finals Champion（每赛季重置）|

---

# Achievement Tiers

Bronze → Silver → Gold → Platinum → Legendary

---

# Key Rules

- **一生一次**：First Slam 解锁后永不重复（赛季类除外）
- **Progress Tracking**：Grand Slams 3/4 → Need Wimbledon（增加目标感）
- **Showcase**：个人主页展示 Recent/Legendary/Favorites/Completion
- **Notifications**：🏆 First Grand Slam Unlocked（Apple 风格/轻量/克制）
- **Timeline 自动关联**：Top100→Achievement→Timeline 无需重复维护
- **AI Achievements**：AI 同样拥有（查看 Federer 也能看到 Career Slam/100 周 No.1）
- **Completion Rate**（未来）：全球 0.8% Players Unlocked（增加收藏价值）

---

# Config Files

achievement.json / achievement_rules.json / tiers.json / hidden.json

---

# Performance

- Achievement Detection <5ms
- Career Query Realtime
- Unlock Animation <16ms

---

# Definition of Done

✓ 自动解锁 ✓ Story 驱动 ✓ 隐藏成就 ✓ AI 同样拥有 ✓ Timeline 自动关联 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

冠军会随着时间被遗忘。成就会提醒玩家：自己曾经走过怎样一段职业生涯。

Achievement System 负责为每一个值得纪念的瞬间留下属于它的一枚勋章。

---

End of Document
