# Ace Career Game Design Document
## Rookie Generation & Talent System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Rookie Generation System（新秀生成系统）负责保证 Ace Career 世界能够持续发展。

随着老球员退役，系统必须持续产生新的职业球员。

世界不会因为时间推移而逐渐没人打球。

每一年都会诞生新的年轻球员。

---

# 2. Design Goal

新秀系统必须满足：

- 世界人口保持稳定
- 每年都有新人
- 每位新人都不同
- AI 与玩家成长规则一致
- 支持无限 Career

---

# 3. Rookie Philosophy

现实 ATP：

每一年都会出现：

- 新秀
- 天才
- 普通球员
- 昙花一现
- 大器晚成

Ace Career 必须模拟这一过程。

不能：

固定生成：

"95 潜力"

玩家。

---

# 4. Rookie Generation Pipeline

```text
Season End
↓
Check Retired Players
↓
Calculate Population
↓
Generate Rookie Pool
↓
Assign Country
↓
Assign Potential
↓
Assign Playing Style
↓
Join Junior Tour
```

---

# 5. Rookie Population

默认：

每年生成：

60~120 名新秀。

数量动态调整：

```text
Retired Players
↓
Population Gap
↓
Generate Count
```

世界人口：

保持：

稳定。

---

# 6. Rookie Age

默认：

生成年龄：

16~18 岁。

少数：

19 岁。

不会：

直接生成：

25 岁新人。

---

# 7. Rookie Potential

Potential：

随机。

但遵循正态分布。

例如：

| Potential | Probability |
|------------|------------:|
| 95~99 | 0.3% |
| 90~94 | 2% |
| 85~89 | 8% |
| 80~84 | 20% |
| 70~79 | 45% |
| <70 | 剩余 |

真正天才：

极少。

---

# 8. Nationality Distribution

国家按照：

真实职业网球人口。

例如：

Spain

Italy

USA

France

Australia

Argentina

Japan

China

Germany

UK

等等。

未来：

支持：

国家兴衰。

---

# 9. Physical Generation

随机生成：

Height

Weight

Dominant Hand

Backhand

例如：

188cm

右手

双反

不会：

所有人：

190cm。

---

# 10. Playing Style

生成：

Aggressive Baseliner

Counter Puncher

Serve Bot

All Court

Clay Specialist

Grass Specialist

风格：

影响成长方向。

---

# 11. Hidden Personality

每位新秀：

拥有：

Professionalism

Discipline

Learning Ability

Work Ethic

Pressure Resistance

Injury Proneness

Consistency

全部：

隐藏。

---

# 12. Talent Labels

极少数球员：

获得：

标签。

例如：

Wonderkid

Late Bloomer

Big Match Player

Iron Man

Glass Body

Hard Court Expert

Clay Monster

这些标签：

长期影响 Career。

---

# 13. Junior Tour

所有新秀：

进入：

Junior Tour。

不是：

直接 ATP。

成长：

达到条件。

自动：

进入 ITF。

---

# 14. AI Development

AI：

自动：

训练。

比赛。

成长。

退役。

所有成长：

完全遵循：

Player Progression。

没有作弊。

---

# 15. Rookie News

真正天才：

自动：

生成新闻。

例如：

```text
17-year-old Japanese prospect wins first ITF title.
```

帮助玩家：

关注未来竞争者。

---

# 16. Rival Generation

若：

年龄相近。

潜力相近。

多次交手。

系统：

自动建立：

Rival。

例如：

未来：

Career Rival。

---

# 17. Data Model

```text
Rookie
PlayerID
Age
Potential
Country
Style
HiddenTraits
CurrentTour
CreatedSeason
```

---

# 18. Edge Cases

支持：

- 黄金一代
- 新秀荒
- 连续多个天才
- 国家崛起
- 国家衰落
- 提前退役

---

# 19. Acceptance Criteria

✓ 每年自动生成新秀

✓ 世界人口稳定

✓ 新秀成长正常

✓ AI 与玩家一致

✓ 支持无限 Career

✓ 世界持续演化

---

End of Document
