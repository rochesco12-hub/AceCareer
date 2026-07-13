# Ace Career Development Bible
# 44 · Media System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Media System 定义整个 Ace Career 的媒体生态系统。

News Engine 负责产生新闻。Media System 负责决定哪些新闻值得持续关注、哪些球员拥有更多曝光、哪些故事会成为热门话题。媒体不是播放器——媒体本身也是职业世界的重要参与者。

---

# Design Goals

✓ 动态关注热点 ✓ Story 驱动 ✓ Reputation + Popularity 双驱动 ✓ AI/玩家一致 ✓ Config Driven ✓ 未来采访系统 ✓ 百年稳定

---

# Media Levels

Local → National → International → Global → Headline

---

# Eight Media Categories

Breaking / Tournament / Feature / Interview / Analysis / Rumor / Historical / Social

---

# Media Score

```
Story Importance + Popularity + Reputation + Tournament Level + Historical Value = Media Score
```

---

# Key Features

- **Breaking Coverage**：No.1 Retires / Grand Slam Champion / Career-ending Injury → 全球头条
- **Feature Story**：Teenage Champion / Comeback Story / Career Journey → 人物专题
- **Tournament Coverage**：Favorites→Upsets→Semis→Final→Champion（持续性报道）
- **Interview Coverage**（未来）：Post Match/Champion/Retirement/Controversy → 影响 Reputation
- **Analysis Coverage**（未来）：Clay Specialist/Serve Improvement/Season Review
- **Social Buzz**（未来）：Epic Match→Trending→Popularity↑（生命周期短于新闻）
- **Exposure**：TV/News/Highlights/Homepage 曝光越高 Popularity 增长越快
- **Media Focus**：每周自动选择 Top Stories/Players/Matches/Narratives（不是平均报道）
- **Bias**（未来）：Home Player/Young Talent/Legend → Coverage+
- **Crisis Coverage**：Long Losing Streak/Major Injury/Coach Split → 媒体持续关注形成压力
- **Media Pressure**（未来）：Headline Every Week→Pressure↑→Mental Fatigue↑
- **Sponsor Connection**：曝光 → Sponsor Value → Contract Offers → Commercial Income
- **World Media**：Top10 Stories→Weekly Headlines→Monthly Review→Season Review（职业世界新闻节奏）
- **Timeline Connection**：Most Covered Match/Historic Interview/Career Documentary

---

# Config Files

media.json / coverage.json / headline.json / importance.json

---

# Performance

- Coverage Update <5ms
- Weekly Media <20ms
- Headline Selection Realtime

---

# Definition of Done

✓ Story 驱动媒体关注 ✓ 自动生成曝光等级 ✓ 支持未来采访系统 ✓ AI/玩家一致 ✓ 商业价值联动 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

冠军决定历史。媒体决定世界如何记住历史。

Media System 让整个职业网球世界真正拥有属于自己的声音。

---

End of Document
