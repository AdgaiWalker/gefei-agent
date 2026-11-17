# SOURCES — 信息来源与处理基线

最后更新：2026-11-16（同步【学员内容】蒸馏：gangbo/gefei-make-money commit 4a9859f、yuanqingsong2024/gefei-quest commit bf4e128；公众号蒸馏基线仍为 20261108，UTC+8）。

## 1. 公众号「哥飞」文章（主来源）
- 已蒸馏到 **2026-11-08** 及以前发布的文章（共约 867 篇）。全部 867 篇（去重后）的日期、标题、原文链接见 [sources/articles-index.md](sources/articles-index.md)，卡片中以 `YYYYMMDD` 引用。
- 2026-11-02 补入 20261029《【哥飞SEO教程】新站外链还要不要买？先在GSC里对比24小时和28天》（GSC 诊断卡、外链卡）；20261101 社群涨价公告只收进索引，不进能力卡。
- 2026-11-09 另补入三篇：20261106《设了 Canonical，谷歌还是收录了复制站》、20261106《哥飞联合谷歌等一起在上海办了一场 AI 出海与增长探索峰会》（只取哥飞本人分享部分）、20261108《花了1.7万美元买外链，没把老站救回来》。
- 部分早期文章文本取自 GitHub 公开导出 [mundane799699/gefei_mp_export](https://github.com/mundane799699/gefei_mp_export)。
- 本仓库**不包含文章正文**，只含提炼后的方法和简短引用。

## 2. GitHub 公开仓库（补充来源）

| 仓库 | 使用的 commit | 用途 | 许可证 |
|---|---|---|---|
| [qiayue/OpenGeFei](https://github.com/qiayue/OpenGeFei)（哥飞本人仓库） | 4b9243a | **一手来源，优先级最高**：guide/ 分步教程，写入各卡「哥飞本人仓库补充」节 | 无 LICENSE 文件（GitHub 未识别许可证）；README 写明“文章版权归哥飞所有，群友故事的原文版权归各位作者所有。欢迎转发和分享这个仓库，转载单篇内容请注明出处并附上原文链接”。本仓库只引用提炼后的方法和简短原话，均注明出处 |
| [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base) | 406c7e3 | 主要补充来源：社群整理的小课堂、案例拆解（逐文件引用路径） | 未声明 |
| [32103210/gefei-seo-guide](https://github.com/32103210/gefei-seo-guide) | 37d6400 | 参考比对（多为公众号复述） | MIT |
| [32103210/gefei-seo-handbook](https://github.com/32103210/gefei-seo-handbook) | fe354f8 | 参考比对 | CC BY-NC-SA 4.0 |
| [Jayin/gefei-seo-cookbook](https://github.com/Jayin/gefei-seo-cookbook) | 0d73d58 | 参考比对 | MIT |
| [hanshan0228/gefei-perspective](https://github.com/hanshan0228/gefei-perspective) | bbd6f76 | 第三方 skill，仅对照 | 未声明 |
| [huodesheng/sitemap-monitor-ext](https://github.com/huodesheng/sitemap-monitor-ext) | 187ce04 | 工具参考（sitemap 监控找新词） | MIT |
| [ifyour/gefei-seo-skill](https://github.com/ifyour/gefei-seo-skill) | 3fea58a | 第三方 skill，仅对照 | MIT |
| [tens1x/gefei-perspective-skill](https://github.com/tens1x/gefei-perspective-skill) | b2a719c | 第三方 skill，仅对照 | MIT（README 声明） |
| [gangbo/gefei-make-money](https://github.com/gangbo/gefei-make-money) | 4a9859f | 学员整理的资料库。既有：哥飞社群外链悬赏帖里署名「哥飞」的评论（外链卡）；哥飞 SEO 工具箱一条标「非哥飞原话/学员整理」（找新词卡）。2026-11-16 增补【学员内容】蒸馏（网页休闲游戏调研、游戏开发 AI Skill/MCP、Ren'Py 网页体积与嵌入、Agent 替代测试），见 [student-gangbo-2026-11.md](gefei/references/practitioner/student-gangbo-2026-11.md) | 未声明 |

**明确排除**：hlwhut225/gefei-knowledge-base 中原文标注"不要外传"的两篇（judgeKey/29、jinjiejiaocheng/01），其任何内容均未收录。

### 哥飞本人仓库 qiayue/OpenGeFei（2026-10-27 接入，2026-11-09 公开）
- 仓库：[qiayue/OpenGeFei](https://github.com/qiayue/OpenGeFei)，分支 main，commit `4b9243a6737824957b937864c9446c0ce2c3be45`，提交时间 2026-09-27 14:04（UTC+8）；2026-11-09 核对远端无新提交。
- 身份核验：GitHub 用户 qiayue 资料 name=gefei、bio=“哥飞”、注册于 2012；README 自述“哥飞 405 篇公众号文章”“文章版权归哥飞所有”，介绍社群 new.web.cafe。判断为哥飞本人账号（可信度高）。
- 许可（2026-11-09 核查）：无 LICENSE 文件，GitHub API 的 license 字段为空；README 写明文章版权归哥飞、群友故事版权归各作者，欢迎转发和分享，转载单篇需注明出处并附原文链接。本仓库不整段转载，只引用提炼后的方法和简短原话，并注明仓库路径。
- 内容：guide/ 15 章分步教程（约 10 万字）；articles/ 405 篇公众号文章（2020–2026-02，与主来源高度重叠）；stories/ 37 篇群友复盘；wall/ 报喜；community/ 社群链接索引。未发现“不要外传”类标注。
- 处理：已读 guide/01、02、03(目录)、04、06、07、10、11、14 相关步骤，写入 7 张独立能力卡和 13 张路由卡的「哥飞本人仓库补充」节。未逐篇读 articles/、stories/、wall/、community/。
- **已发现的更正**：“上付费→涨价→上订阅→上年付”四阶段出自群友 Lucas小杨 文章（哥飞转载认同），不是哥飞本人原创方法论；新站“先免登录免费用”（哥飞 2025-01-13）优先于群友“改成必须付费才出单”的经验。

## 3. 公开流传的哥飞群聊截图
- 2026-10-04（ChatGPT/GEO 推荐流量）、2026-10-22（技能链、Sprunki 商标、月入万刀算账、新词量级、adsterra 广告）、日期未知·[与刘小排的分工定位](sources/group-chat/刘小排分工.md)。哥飞本人发言文字见 [sources/group-chat/](sources/group-chat/)；未收录截图原图和其他群友发言。2026-10-22 Sprunki 一段截图不完整。
- 哥飞本人表示是猜测的内容标为【推测】。

## 4. 哆啦的笔记（个人整理，非哥飞原话）
- [西门出海经验，哆啦 2026-10-27 整理](gefei/references/practitioner/ximen-2026-10-27.md)：第三方实战经验（选词、建站模板、定价与成本、收款、长期运营）。引用时单独标注，与哥飞观点分开写，冲突时以哥飞为准。
- 公开前已删去原笔记「待办」一节（含第三方人名与联系方式转介）；未发现标注"不要外传"或付费会员专属的内容。

## 5. 学员内容（非哥飞原话，2026-11-16 起默认同步）
- [gangbo/gefei-make-money 2026-11 蒸馏](gefei/references/practitioner/student-gangbo-2026-11.md)：来源仓库 commit `4a9859f`（2026-11-13）。含网页休闲游戏热度调研方法与机会判断、游戏开发 AI Skill/MCP 选型、Ren'Py 网页体积与嵌入、Agent 替代测试。
- [yuanqingsong2024/gefei-quest 2026-11-10～16 蒸馏](gefei/references/practitioner/student-gefei-quest-2026-11.md)：来源仓库 commit `bf4e128`（2026-11-16）。含 GEO/AEO checklist，以及 ai-wool、github-finds、money-rank、agent-money、opc-briefs 的快照要点。
- 引用规则：单独成段，标「学员内容」，不得混作哥飞原话；与哥飞冲突时以哥飞为准。数字下结论前须重查。
- **公开同步规则**（2026-11-16 起）：标注为「学员内容」的蒸馏默认同步到本仓库；原文标注"不要外传"或付费会员专属的内容、密钥和个人信息不同步。

## 6. 本队执行规则（工程约束，非哥飞原话）

- [本队判词执行规则 2026-11-17](gefei/references/practitioner/team-keyword-rules-2026-11-17.md)：本队做新词站流水线时，于 2026-11-10 试跑后自己定的 5 条兜底约束（阈值不凑数、数据缺失不给满分、文案不许含糊、同名干扰最多观察、打分来源必须披露）。
- 性质：**工程约束，不是哥飞说过的话**。依据是本队内部《流水线试跑问题修复单》与《规则表》，非哥飞原文。
- 引用规则：单独成段并标「本队规则」，不得混作哥飞口径；与哥飞原话冲突时以哥飞为准。
- 前四条对应哥飞判词卡已有的口径（三分结论、意图一致性），属落地兜底；第五条（打分来源与判分标准公开）是本队新增的透明度要求，哥飞原文未涉及。

## 7. 校验
用 cangjie-skill 的 `scripts/validate_skill_pack.py <本仓库路径>` 校验，应为 0 errors。

## 读者反馈
- 2026-10-28 · X [@growaiskills](https://x.com/growaiskills/status/2115111506060701768)：建议每条经验附原文日期和适用条件，判词时重查近期搜索量和搜索结果页。已采纳：GitHub 来源补原文发布日期；判词/找新词/变现定价/竞品研究四张卡加「数据时效规则」。
- 2026-10-28 · X [@yikun900655](https://x.com/yikun900655/status/2115263205782299124)：判词第 4 条「回报」没讲清楚。已采纳：判词卡「回报」加使用提醒并指向变现定价卡。
