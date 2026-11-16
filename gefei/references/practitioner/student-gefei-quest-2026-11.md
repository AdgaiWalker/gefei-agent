# 学员内容：yuanqingsong2024/gefei-quest 2026-11-10～16 增量蒸馏

> **【学员内容】非哥飞原话。** 来源仓库 [yuanqingsong2024/gefei-quest](https://github.com/yuanqingsong2024/gefei-quest)。本轮处理到 commit `bf4e128f829da4aa942ecd9db5f87b6025d63e79`（提交时间 2026-11-16 10:10，北京时间），范围为基线 `af79092` 之后的新增。引用时必须标注「学员内容」，不得混作哥飞原话；与哥飞冲突时以哥飞为准。
>
> 数据时效：羊毛、分成、标价、促销截止日期都是日更快照，使用前须核对官方页面。不要把快照数字写成承诺。

## 1. GEO / AEO checklist（starter）

来源：`starters/geo-checklist/`（清单补全自 commit `eabf7da`，2026-11-10；仓库本轮基线 `bf4e128`）。这是英文练站单页模板，不是已上线的审计产品。作者同时改了 `starters/aeo-checklist/` 的缺口，方法与本节合并蒸馏。

**概念**

- 经典 SEO、AEO、GEO 标签重叠，不是三选一：先复用可抓取、实体一致、把话写清楚，再改「测什么」和「怎样把结论写成可被引用的结构」。
- 不要编造「官方 GEO 分数 / citation rate」，也不要承诺流量或 AI 引用。

**可执行清单（蒸馏）**

- 抓取与访问：robots / meta 放行要被发现的页；修软 404、错误 canonical 和钱页孤岛；关键内容写在 HTML 里，不要只靠空壳客户端渲染。若走 ChatGPT 搜索或浏览，robots 放行 `OAI-SearchBot` 与 `ChatGPT-User`，并用对应 User-Agent curl，确认 HTTP 200 且 h1、正文已在 HTML 中。训练型爬虫是否放行要单独决定。
- 先给答案、再对齐实体：每个主查询在 H1 下先写 2–4 句直接回答；品牌 / 产品 / 作者名称全站和公开资料拼写一致；敏感主张写明作者、更新日期和经验依据。
- 意图对应页型（五类，各指定一个主页型）：找工具、找替代、how-to、事实 / FAQ、值不值得（worth-it）。「Best free X / X tool」要落到带可用表单的工具或对比页，不要只写长文；「X alternatives」走替代页；「How to X」走指南（先服务谷歌搜索），有工具再链过去；事实题在同一 URL 给直接回答 + FAQ；「Is X worth it」用带可辩护数字的指南。
- 工具 / 生成器页：一个 URL 只做一件具体任务；首屏就能开始用；H1 下第一句写清是什么、给谁、免费还是付费、要不要注册；FAQ 约 10 条且每条第一句先给结论；价格和限制在首页、定价页、FAQ、JSON-LD 上必须一致；只写已经上线的功能。上线当天把 URL 写入 sitemap、llms.txt，并从首页或工具索引内链过去。
- 结构与 schema：一个 H1，H2/H3 跟着真实问题走；FAQ / Article / HowTo 等标记只在可见正文确实是该类型时才加，并做校验。
- 可辩护的测量：继续用 Search Console 看查询、页面和覆盖；每月抽查 5–10 个优先问题在 AI 回答界面里是否出现、描述是否准确，并另开对话保存原始回复。分析里把 AI 助手引荐从 Direct / Referral 里分开，不要混进 organic，也不要把 Cloudflare 与 GA4 加总。抽查提示词示例：「What's the best free [category] tool?」「[Competitor] alternatives」「Can you visit [your domain] and tell me what it does?」「Would you recommend [your domain]? What would it need to improve?」

## 2. 日更数据快照（2026-11-10～16）

只收有方法或可复用信息的部分，不整表搬迁。数字一律视为当时快照。

### ai-wool（AI 羊毛 / 免费额度）

来源：`data/ai-wool/2026-11-10.json`～`2026-11-16.json`。这是会过期的促销和免费档追踪，技能包不把它当长期建议。本周可见的类型包括：限时促销、免费额度、Token 福利、订阅折扣、学生教育。代表性条目（使用前核对官方，部分窗口可能已关闭）：

- 2026-11-10：Claude Fable 5.2 上线周限时额度；蚂蚁百灵 Ling-3.2-flash API 限时免费（约至 11/19）；Kiro Students、Mistral Education 等学生档。
- 2026-11-11：OpenCode Console 限时免费模型；Inception Mercury 3 新账号一次性免费 Token；Google Cloud Express Mode、Google Vids 免费层。
- 2026-11-12：MiniMax 生图限时折扣（至 11/18）；Gemini 付费 API 导入期半价（至 11/30）。
- 2026-11-16：Gemini 4 Hydrogen 免费档；Google AI Studio 订阅积分领取；讯飞 SparkAudio 个人实名免费包；Vercel AI Gateway / Token Pass 当时优惠。

### github-finds（GitHub 发掘）

来源：`data/github-finds/2026-11-10.json`～`2026-11-16.json`。本周方法是按日分类发掘，并给「可执行的跟做步骤」，不是只贴仓库名。

- 工作日偏「项目」类（可借鉴的开源实现、技能 / Agent 相关工具）。
- 周末偏「生活」类（家庭提醒、固定支出体检等可落地小工具）。
- 本周约 31 条，其中生活向 16、项目向 15。具体仓库星数和用途会变，需要的话回原仓库按日期查，不要把清单当永久推荐。

### money-rank（赚钱路径榜）

来源：`data/money-rank/2026-11-10.json`～`2026-11-13.json`（11-14～16 无新文件）。这是学员整理的路径清单，分成比例以各平台官方条款为准，技能包不背书收益。

本周反复出现的类型：联盟营销（建站 / 主机教程类联盟）、数字产品与接单（Gumroad、Payhip 等）、出海小站（先用 Cloudflare Pages 验证流量再接广告或联盟）、平台激励、素材投稿、闲鱼非实物技能服务、盯新品目录做「是什么 / 替代品」单页、案例拆解。费率、Cookie 时长和结算周期必须重查官方，页面写的「约 xx%」不能直接当现行规则。

### agent-money（Agent 变现渠道）

来源：`data/agent-money/2026-11-12.json`、`2026-11-16.json`。学员对照的是「上架技能 / MCP / 可雇 Agent」一类货架，分成和提现规则以官方条款为准。

当时整理到的渠道类型包括：Skillzy（技能 / Agent 配置，约 80%，Stripe Connect）、MCP Marketplace（付费 MCP，约 85%）、Toku.agency（可雇 Agent 服务，完成后约 85% 入钱包）、SkillHQ（付费 SKILL.md，Starter 约 80% / Pro 约 85%）、扣子技能商店（国内支付宝 / 抖音支付结算）、Agensi（MCP 分发，约 70%，Stripe 仅限部分国家）、MCPize（付费 MCP 服务器，订阅约 80%，每月 1 日打款）。另有个别案例拆解和闲鱼「上架对照手册」方案。国家限制、审核、冻结期和平台费率变化快，引用前必须打开官方文档。

### opc-briefs（国内经营合规简报）

来源：`data/opc-briefs/2026-11-10.json`、`2026-11-12.json`、`2026-11-14.json`。这是学员对公开政策的摘录，不是法律意见；执行以官方原文和当地口径为准。

- 2026-11-10：小规模纳税人增值税按季计税，起征点为季度销售额 30 万元（按月 10 万元），材料称执行至 2027 年底；未达免征，达到则全额计税，并可减按 1% 征收率。来源：[国家税务总局相关政策页](https://fgk.chinatax.gov.cn/zcfgk/c102416/c5247434/content.html)。
- 2026-11-12：一人公司须备案受益所有人；注册资本不超过 1000 万元、股东均为自然人且无股权外控制或收益安排的，可承诺免报。来源：[中国政府网相关政策页](https://www.gov.cn/zhengce/202405/content_6949955.htm)。
- 2026-11-14：已登记的网络交易经营者须在网站首页或经营主页显著位置持续公示执照信息或链接，可接入总局电子营业执照亮照系统；信息变更后 10 个工作日内更新。来源：[市场监管总局相关政策页](https://www.samr.gov.cn/zw/zfxxgk/fdzdgknr/fgs/art/2025/art_4b47c79b8d994a42bba4835997688faa.html)。

## 本轮未展开的提交

- `content(ai-life)` 置顶选题（双 11 购物参谋、家庭健康档案参谋、冰箱清库存参谋）：属于该练站营的内容选题记录，不是可复用方法论，未单独成节。
- `chore(weekly)` 等同步脚本、页面 embed 回退：工程维护，不进技能包。
- 2026-11-09 基线 `af79092` 及更早的学员榜单、羊毛、闲鱼执行包等，仍维持此前「未整篇收录」的处理，本轮只收 11-10 起的蒸馏。
