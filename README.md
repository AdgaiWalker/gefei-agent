# 哥飞 Agent（非官方）

把公众号「哥飞」公开分享的出海新词站 / SEO / GEO 方法论，蒸馏成 AI Agent 能直接调用的技能（Skills）。装好后，你用大白话提问，Agent 会按哥飞的方法回答，并注明出自哪篇文章或哪天的群聊。

## 能力列表（13 张能力卡）

| 能力卡 | 解决什么 |
|---|---|
| `gefei-first-site-roadmap` ★ | 第一个出海站怎么规划、练手站做到什么程度、月入目标倒推 |
| `gefei-keyword-discovery` ★ | 找新词、挖需求 |
| `gefei-keyword-evaluation` ★ | 这个词能不能做、KGR/KD、商标风险 |
| `gefei-intent-site-structure` ★ | 搜索意图、网站结构、URL 与内链 |
| `gefei-onpage-launch` ★ | 站内 SEO、上线、提交收录 |
| `gefei-gsc-diagnosis` ★ | 不收录、掉排名、GSC 提示怎么看 |
| `gefei-monetization-pricing` ★ | 变现方式、订阅定价、有流量没订单 |
| `gefei-backlinks-promotion` | 新站外链、社区推广 |
| `gefei-programmatic-pages` | 程序化 SEO、日更数据页 |
| `gefei-multilingual` | 多语言、小语种关键词 |
| `gefei-site-portfolio` | 长期养站、有排名后横向扩展 |
| `gefei-competitor-research` | 估算竞品收入、关联站长、域名历史 |
| `gefei-chatgpt-traffic` | 从 ChatGPT 拿推荐流量（GEO） |

★ = 独立 Skill（`gefei-*/` 目录）；其余在路由 Skill `gefei/references/capabilities/` 里，由 `gefei` 按意图自动加载。

## 1. 选环境

任何支持 `SKILL.md` 规范的 Agent 都能用。按你手上的工具选：

| 环境 | 全局技能目录（所有项目可用） | 项目内目录 |
|---|---|---|
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| Cursor | `~/.cursor/skills/`（也读 `~/.agents/skills/`、`~/.claude/skills/`） | `.cursor/skills/` 或 `.agents/skills/` |
| Codex CLI | `~/.agents/skills/`（旧版 `~/.codex/skills/` 也能读） | `.agents/skills/` |
| 其他 Agent | 不认识 skills 目录时，直接让它读 `gefei/SKILL.md` | — |

路径依据：[Claude Code Skills](https://docs.claude.com/en/docs/claude-code/skills)、[Cursor Agent Skills](https://cursor.com/docs/skills)、[Codex Skills](https://learn.chatgpt.com/docs/build-skills.md)。

## 2. 安装

一共 8 个技能目录：`gefei`（路由）+ 7 个 `gefei-*`。推荐 clone 到固定位置再软链接，以后 `git pull` 一下就更新。

### Claude Code

```bash
git clone https://github.com/AdgaiWalker/gefei-agent ~/gefei-agent
mkdir -p ~/.claude/skills
for d in ~/gefei-agent/gefei ~/gefei-agent/gefei-*/; do ln -sfn "${d%/}" ~/.claude/skills/; done
ls ~/.claude/skills | grep gefei
```

或者直接把这段话发给 Claude Code：

```text
帮我把 https://github.com/AdgaiWalker/gefei-agent 安装成全局 skill：clone 到 ~/gefei-agent，然后把仓库里的 gefei 目录和所有 gefei-* 目录软链接到 ~/.claude/skills/，装完列出已安装的 gefei 相关 skill。
```

### Cursor

```bash
git clone https://github.com/AdgaiWalker/gefei-agent ~/gefei-agent
mkdir -p ~/.cursor/skills
for d in ~/gefei-agent/gefei ~/gefei-agent/gefei-*/; do ln -sfn "${d%/}" ~/.cursor/skills/; done
ls ~/.cursor/skills | grep gefei
```

在 Cursor 的 Agent 对话框里发：

```text
帮我把 https://github.com/AdgaiWalker/gefei-agent 安装成 Cursor 全局 skill：clone 到 ~/gefei-agent，把 gefei 目录和所有 gefei-* 目录软链接到 ~/.cursor/skills/，装完列出来，并告诉我是否需要重开窗口。
```

### Codex CLI

```bash
git clone https://github.com/AdgaiWalker/gefei-agent ~/gefei-agent
mkdir -p ~/.agents/skills
for d in ~/gefei-agent/gefei ~/gefei-agent/gefei-*/; do ln -sfn "${d%/}" ~/.agents/skills/; done
ls ~/.agents/skills | grep gefei
```

在 Codex 里发：

```text
帮我把 https://github.com/AdgaiWalker/gefei-agent 安装成 skill：clone 到 ~/gefei-agent，把 gefei 目录和所有 gefei-* 目录软链接到 ~/.agents/skills/，装完列出来。
```

> Windows 不方便软链接的话，把 `ln -sfn` 换成复制（`cp -r`），更新时重新复制一次。

### 其他 Agent（没有 skills 机制）

```text
请先读取 https://github.com/AdgaiWalker/gefei-agent 仓库里的 gefei/SKILL.md，以后我问出海建站、SEO、找词、变现的问题时，按它的路由表加载对应的能力卡来回答，并注明来源。
```

## 3. 验证安装

新开一个对话，发：

```text
你现在有哪些哥飞相关的 skill？用一句话分别说明，并告诉我"哥飞的核心原则"有哪几条。
```

能列出 `gefei` 和 7 个 `gefei-*`，并说出"搜索量来自共识""一个关键词一个页面"之类的原则，就装好了。Claude Code / Cursor 里也可以输入 `/gefei` 手动调用。

## 4. 使用：按阶段复制提示词

把 `【】` 里的内容换成你自己的情况。

**找新词 / 需求挖掘**
```text
用哥飞的方法，帮我找 【AI 图片工具】 方向最近出现的新词：告诉我去哪些渠道找、每一步怎么操作，并给出今天就能动手的清单。
```

**判词（能不能做）**
```text
按哥飞的判词方法评估这几个关键词能不能做：【词1】【词2】【词3】。逐个看搜索量趋势、intitle/KGR、KD、前排是首页还是内页、商标风险，最后排序给结论。
```

**第一个站路线**
```text
我是新手，会一点前端，每天能投入 3 小时。按哥飞的思路，帮我规划第一个出海练手站：做到什么程度算合格、多久上线、之后怎么滚到月入万刀。
```

**建站结构 / 搜索意图**
```text
关键词是 【xxx generator】。按哥飞的方法分析它的搜索意图，给我设计网站结构：首页放什么、需要哪些内页、URL 怎么定、内链怎么连。
```

**站内 SEO 与上线**
```text
我的站 【域名】 准备上线。按哥飞的上线清单检查 Title/Description/H1、提交收录的步骤，以及新站上页面的节奏。
```

**外链与推广**
```text
新站刚上线，0 外链。按哥飞的方法给我一份前 30 天的外链和推广计划：先做哪些、哪些别做。
```

**GSC 诊断**
```text
我的站上线两周，GSC 显示"已抓取 - 尚未编入索引"，展示量从 500 掉到 50。按哥飞的诊断思路帮我排查原因，并给出修复顺序。
```

**ChatGPT / GEO 流量**
```text
按哥飞关于 ChatGPT 推荐流量的观点，我的新词工具站要怎么写页面文案、怎么验证有没有拿到 GPT 流量？哪些是他的推测要标出来。
```

**变现定价**
```text
我的工具站日均 800 UV，还没订单。按哥飞的方法帮我选变现方式、定订阅价格，并按"有流量没订单先修漏斗"排查。
```

**竞品研究**
```text
帮我按哥飞的方法研究竞品 【competitor.com】：估算流量和收入、看它的外链和关联站、查域名历史，判断这个方向值不值得跟。
```

**程序化 SEO / 多语言 / 养站**
```text
我的站有了第一批排名。按哥飞的方法判断下一步该做程序化页面、加多语言，还是横向再开新站？
```

### 完整示例：新人从 0 到第一单

> **你**：我是新手，想按哥飞的方法做第一个出海站，从找词开始一步步带我。
> **Agent**（first-site-roadmap）：先定目标：练手站目标是"上线 + 拿到第一批谷歌流量"，不求完美……第一步去找新词。
>
> **你**：好，帮我找词，我对 AI 图片方向感兴趣。
> **Agent**（keyword-discovery）：去 Google Trends 看近 7 天飙升词、看新站 sitemap……给你 5 个候选。
>
> **你**：这 5 个哪个能做？
> **Agent**（keyword-evaluation）：逐个算 KGR、看 KD 和前排……第 2 个前排都是内页、有趋势、无商标风险，推荐它。
>
> **你**：网站该怎么搭？
> **Agent**（intent-site-structure + onpage-launch）：一个关键词一个页面，首页就是工具本身……Title 这样写，上线后提交 GSC。
>
> **你**：上线 3 天了，有展示没点击，也没 ChatGPT 流量。
> **Agent**（gsc-diagnosis + chatgpt-traffic）：先看 Title 是否命中意图……工具页文案要直接回答用户会在 ChatGPT 问的问题（哥飞观点，部分为【推测】）。
>
> **你**：每天 300 UV 了，怎么赚钱？
> **Agent**（monetization-pricing）：先算账：客单价 40 美元、1% 付费率……先上订阅，定价参考……
>
> **你**：出了第一单！下一步？
> **Agent**（site-portfolio / first-site-roadmap）：复盘这套流程，再开下一个新词站，用练手站逐级跑通……

## 5. 更新

```bash
cd ~/gefei-agent && git pull
```

用软链接安装的，pull 完就生效；用复制安装的，要重新复制一次。也可以直接让 Agent 做：

```text
帮我更新哥飞 skill：在 ~/gefei-agent 里 git pull，然后告诉我这次更新改了哪些能力卡、哥飞有没有改变说法。
```

## 6. FAQ

**【推测】是什么意思？**
哥飞本人明确说"我猜""我怀疑""我的推断"的内容，标成【推测】，不要当成定论。

**怎么查某条说法的出处？**
每条都写了来源：公众号文章用日期 `YYYYMMDD` 标注，到 [sources/articles-index.md](sources/articles-index.md) 按日期查标题和原文链接；GitHub 来源写了仓库和文件路径；群聊内容见 [sources/group-chat/](sources/group-chat/)。也可以直接问 Agent："这条出自哪里？"

**这是哥飞本人做的吗？**
不是。这是非官方整理，与哥飞无关，也没有得到他的背书。理解可能有偏差，以哥飞原文为准。想系统学习请关注公众号「哥飞」。

**答案和最新情况不一样？**
内容截止到 2026-10-26 的文章。先 `git pull` 更新；仍不一致，欢迎提 issue。

---

## 非官方声明

> ⚠️ **非官方项目**：本仓库与哥飞本人无关，未经哥飞授权或背书。内容是对公开资料的个人整理与提炼，可能有误读；以哥飞原文为准。本仓库**不包含文章正文**，只含提炼后的方法和简短引用，每条都注明出处。

## 信息来源

详见 [SOURCES.md](SOURCES.md)。

1. **公众号「哥飞」**（主来源）：2019–2026-10-26 的公开文章。全部 862 篇文章索引（日期、标题、原文链接；585 篇有 mp.weixin 链接）见 [sources/articles-index.md](sources/articles-index.md)。部分早期文章文本取自 [mundane799699/gefei_mp_export](https://github.com/mundane799699/gefei_mp_export)（未声明许可证）。
2. **GitHub 公开仓库**：

| 仓库 | 许可证 | 本仓库如何使用 |
|---|---|---|
| [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base) | 未声明 | 主要补充来源，逐条注明文件路径 |
| [32103210/gefei-seo-guide](https://github.com/32103210/gefei-seo-guide) | MIT | 仅参考比对 |
| [32103210/gefei-seo-handbook](https://github.com/32103210/gefei-seo-handbook) | CC BY-NC-SA 4.0 | 仅参考比对，未摘录内容 |
| [Jayin/gefei-seo-cookbook](https://github.com/Jayin/gefei-seo-cookbook) | MIT | 仅参考比对 |
| [hanshan0228/gefei-perspective](https://github.com/hanshan0228/gefei-perspective) | 未声明 | 仅对照 |
| [huodesheng/sitemap-monitor-ext](https://github.com/huodesheng/sitemap-monitor-ext) | MIT | 工具参考 |
| [ifyour/gefei-seo-skill](https://github.com/ifyour/gefei-seo-skill) | MIT | 仅对照 |
| [tens1x/gefei-perspective-skill](https://github.com/tens1x/gefei-perspective-skill) | MIT（README 声明） | 仅对照 |

3. **公开流传的哥飞群聊截图**（2026-10-04、2026-10-22）：哥飞本人发言的文字整理见 [sources/group-chat/20261004.md](sources/group-chat/20261004.md)、[sources/group-chat/20261022.md](sources/group-chat/20261022.md)；不含截图原图与其他群友发言。

卡片里的补充小节都标明来源，例如「补充（来源：GitHub hlwhut225/gefei-knowledge-base）」「补充（来源：公开流传的哥飞群聊截图 2026-10-22）」。哥飞本人说是猜测的内容标为【推测】。原文明确标注"不要外传"的资料未收录。

## 许可证

本仓库的整理与提炼内容以 [CC BY-NC 4.0](LICENSE) 发布（署名-非商业性使用）。被引用观点的原始著作权归哥飞及各原作者所有。

## 删除请求

如哥飞本人或任何原作者希望删除或修改相关内容，请提 issue，我们会尽快处理。
