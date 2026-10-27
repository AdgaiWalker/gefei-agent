# 哥飞 Agent（非官方）— 出海新词站 / SEO / GEO 方法论技能包

把公众号「哥飞」公开分享的方法论蒸馏成一组可执行的 Agent 技能（skills）：选新词、判词、搜索意图与网站结构、站内 SEO 与上线、GSC 诊断、外链推广、程序化 SEO、多语言、养站、竞品收入侦察、ChatGPT/GEO 推荐流量、变现定价。

> ⚠️ **非官方项目**：本仓库与哥飞本人无关，未经哥飞授权或背书。内容是对公开资料的个人整理与提炼，可能有误读；以哥飞原文为准。本仓库**不包含文章正文**，只含提炼后的方法和简短引用，每条都注明出处。

## 能力列表

| Skill / 能力卡 | 用途 |
|---|---|
| `gefei`（路由入口） | 总览、术语、速查，并按意图路由到下面的能力卡 |
| `gefei-first-site-roadmap` | 第一个出海站、练手站、月入目标倒推 |
| `gefei-keyword-discovery` | 找新词、挖需求 |
| `gefei-keyword-evaluation` | 判断词能不能做、KGR/KD、商标风险 |
| `gefei-intent-site-structure` | 搜索意图、网站结构、URL 与内链 |
| `gefei-onpage-launch` | 站内 SEO、上线、提交收录 |
| `gefei-gsc-diagnosis` | 收录与排名问题诊断 |
| `gefei-monetization-pricing` | 变现方式、订阅定价、漏斗排查 |
| 路由卡：backlinks-promotion / programmatic-pages / multilingual / site-portfolio / competitor-research / chatgpt-traffic | 见 `gefei/references/capabilities/` |

## 使用方法

每个目录（`gefei/`、`gefei-*/`）都是一个标准 `SKILL.md` 技能：

- **Claude Code**：把这些目录复制到 `~/.claude/skills/`（或项目内 `.claude/skills/`）。
- **Cursor / 其他支持 Agent Skills 的工具**：复制到对应的 skills 目录，或在规则里引用 `gefei/SKILL.md`。
- **任意 Agent**：把 `gefei/SKILL.md` 作为系统提示入口，按其中路由表按需读取 `references/capabilities/*.md`。

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
