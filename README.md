# 哥飞 Agent（非官方）

把公众号「哥飞」公开分享的出海新词站 / SEO / GEO 方法论，做成 AI 能直接用的技能。装好后用大白话提问，AI 按哥飞的方法回答，并注明出处。

**定位（哥飞原话）**：小排老师教你做产品；哥飞教你怎么找到可以做产品的需求，以及做出产品后怎么推销出去赚到钱。

## 安装只要一句话

打开 **Claude Code / Cursor / Codex**（或任何能执行命令的 AI Agent），粘贴：

```text
帮我安装 https://github.com/AdgaiWalker/gefei-agent
```

AI 会自己读下面的安装说明并装好。

> 网页版聊天工具（ChatGPT 网页、Claude 网页等）不能执行命令，装不了。

## 装好后这样用

```text
用哥飞的方法，帮我找 AI 图片方向最近的新词
```
```text
按哥飞的判词方法，看看 【xxx generator】 这个词能不能做
```
```text
我是新手，按哥飞的思路帮我规划第一个出海站
```
```text
我的站不收录、掉排名了，按哥飞的方法帮我排查
```
```text
按哥飞的观点，新站怎么拿 ChatGPT 推荐流量？
```

<details>
<summary>更多场景提示词（11 个阶段）</summary>

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

</details>

<details>
<summary>能力列表（13 张能力卡）</summary>


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

</details>

## 更新

对 AI 说：`帮我更新哥飞 skill`（AI 会在 ~/gefei-agent 里 git pull）。

## 给 AI 的安装说明（用户不用看）

AI Agent 请按以下步骤执行：

1. 判断你是哪个 Agent，确定技能目录：Claude Code → `~/.claude/skills`；Cursor → `~/.cursor/skills`；Codex CLI → `~/.agents/skills`；不确定时用 `~/.agents/skills`。
2. 克隆（已存在则 `git -C ~/gefei-agent pull`）：
   ```bash
   git clone https://github.com/AdgaiWalker/gefei-agent ~/gefei-agent
   ```
3. 把 `gefei` 和所有 `gefei-*` 目录放进技能目录（`SKILLS` 换成第 1 步的路径）：
   ```bash
   SKILLS=~/.claude/skills; mkdir -p "$SKILLS"
   for d in ~/gefei-agent/gefei ~/gefei-agent/gefei-*/; do ln -sfn "${d%/}" "$SKILLS/"; done
   ```
   Windows：不用软链接，把这 8 个目录复制（`Copy-Item -Recurse`）到 `%USERPROFILE%\.claude\skills` 等对应目录。
4. 验证：`ls "$SKILLS" | grep gefei` 应列出 `gefei` 和 7 个 `gefei-*`（共 8 个），且 `$SKILLS/gefei/SKILL.md` 存在。
5. 告诉用户"哥飞 Agent 已安装"（如需重开窗口请提醒），并给出 3 个示例：
   - 用哥飞的方法，帮我找 AI 图片方向最近的新词
   - 我是新手，按哥飞的思路帮我规划第一个出海站
   - 按哥飞的观点，新站怎么拿 ChatGPT 推荐流量？

用户说"更新哥飞 skill"时：`git -C ~/gefei-agent pull`；复制安装的需重新复制，并概述改了哪些能力卡。

## 常见问题

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
