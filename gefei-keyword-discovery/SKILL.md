---
name: gefei-keyword-discovery
description: |
  当不知道做什么站、要找新词/蓝海词/有搜索需求的关键词、某个新模型/新游戏/新梗火了想蹭、或想从同行/竞品发现机会时使用。产出带来源和趋势的候选词清单。判断某个具体词值不值得做请用 gefei-keyword-evaluation。
metadata:
  cangjie.generated-by: cangjie-tools v2.5.0
  cangjie.capability-id: cap.gefei.keyword-discovery
  cangjie.capability-revision: 1
  cangjie.bundle-id: bundle.gefei
  cangjie.source-title: 「哥飞」公众号文章合集（2019–2026，862篇）
  cangjie.tags: 哥飞, 出海, SEO
---
<!-- capability_id: cap.gefei.keyword-discovery | revision: 1 | status: active -->

# 找新词与找需求：从共识里挖有人搜、少人做的词

> **数据时效规则（2026-10-28 加，采纳 X 用户 @growaiskills 的反馈）**：本卡的方法可以复用，但引用原文里的搜索量、KD/竞争、CPC、价格、收入、外链数等都是**当时的历史数据**，出处旁已标原文发布日期。下结论前要按当前重查：近期搜索量（Google Trends / Ads 关键词规划师）、当前搜索结果页前 10、当前竞品价格；必要时注明适用条件（时间、市场/语种、站点类型）。数据对不上时，以重查结果为准，方法不变。

## R — 原文 (Reading)

> 新词竞争度低，参与竞争的网站少，大家都在同一条起跑线上，所以你只要……做到比你的竞争对手更好，谷歌就会把你排到前面。
>
> — 哥飞，《新网站上线最快多久能从谷歌获取搜索流量？》(20230904)

> 搜索量来自于共识。
>
> — 哥飞，《【哥飞SEO理论】搜索量来自于共识》(20250421)

## I — 方法论骨架 (Interpretation)

需求 = 有足够多人用**同一种表达**去搜（共识），而参与竞争的网页还少。找词就是系统地扫描"新出现的共识"：

- **新词**：出现不超过约 12 个月（谷歌趋势看起点）；谷歌称每天约 15% 搜索是新的，新需求源源不断。
- **蓝海词**：不新，但 intitle 供应量少、热度在涨（交给判词卡量化）。
- **渠道（由易到难）**：
  1. 谷歌趋势：看"上升"相关查询、和基准词（如 GPTs）对比热度、拉长时间看起点与季节性；
  2. 种子词根组合：Generator / Converter / Calculator / Checker / Maker / Translator 等"财富密码"词根 + 新事物名（新模型、新游戏、新梗）；
  3. 站找站 / 站找词 / 词找站 / 词找词：从好站的相似站、出站域名、排名词扩展；
  4. Sitemap 盯同行：5–20 个活跃同行的 sitemap 定期 diff，新 URL 就是别人刚发现的词；
  5. 看正在投广告的产品：Similarweb 付费词里的需求词 + 落地页成交路径 = 被验证的可付费需求；
  6. 下拉框、YouTube/TikTok/Pinterest、Reddit 等用户表达。
- 动手前三查：需求是否明确？现有结果是否已经满足？我能否做得更好/更快？

### 补充（来源：GitHub [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base)，2026-10-27 整理）
- **谷歌趋势找新词（哥飞小课堂 2024-08-13）**：判新词时依次看 30 天、90 天、12 个月、5 年曲线，曲线起点就是该词的出现日期，30 天内出现最好。扩词时输入词根，选全球、最近 7 天，看"相关查询"，也留意拼写错误词（ChatTTS→ChaTTS）；用产品名或品类名递归扩（AI Music→udio→suno）；可以接 Google Trends API 自动化；在"网站↔词↔更多词↔更多网站"之间循环。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 jinjiejiaocheng/06-guge-qushi-zhao-xinci.md（原文发布 2024-08-13）
- **根词列表维护（群友"睡觉想飞"整理哥飞"8 种找词方式"，2025-04-13，转述）**：把可能的根词存成列表，按 7 天或 30 天周期去 Trends 查，能扩出新词的保留，否则淘汰。已在公众号公开、域名已被大量注册的词不建议做。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 xuqiuwajue/19-xiaobai-zenme-zhaoci.md（原文发布 2025-04-13）（"8 种找词方式"的原文 web.cafe/tutorial/detail/lmlpg7ae96 未见于任何仓库）
- **时间分配（群友卡诺转述哥飞，2024-12-27）**：约 40% 时间挖需求、20% 开发、40% 推广做外链。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 xuqiuwajue/18-manyou-zhao-ci-sop.md（原文发布 2024-12-27）

### 补充·第二批（来源：GitHub [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base)，小课堂与案例拆解，2026-10-27 整理）
- **新词玩法的三个层级（小课堂 2025-08-10）**：初级是跟进，别人上什么页面你就上什么；中级是预测，提前注册可能会火的词并占坑；高级是创造，自己造出新词再拿走大部分流量（higgsfield 的 Earth Zoom Out）。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/54-i33t7dyhxb.md（原文发布 2025-10-10）
- **新词由社交媒体造（案例 2024-12-08）**：关注 TikTok 等社交媒体可以发现新词。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/28-08zfe1fbve.md（原文发布 2025-10-29）
- **从大站关键词和改版史里找词（案例 2025-01-14）**：研究有流量网站的关键词列表；从任意关键词的搜索结果里，都可能挖到值得研究的网站。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/45-qxza0rekyl.md（原文发布 2025-10-11）
- **挖需求方法汇总（小课堂《再聊挖掘需求的方法》）**：① 词根扩展（51 个词根 × Semrush Keyword Magic Tool 筛选，再用 Trends 和 Ads 规划师核实搜索量）；② 查 SEO 大站的流量关键词，重点看"别人只靠内页就拿下"的词，以及 Similarweb 里"新获得点击"的页面；③ 谷歌下拉词；④ 把前三种组合起来循环；⑤ 看有人持续在投广告的关键词（qr code generator 案例，"别人一直投广告，说明一直在赚钱"）；⑥ 从变现角度找正在赚钱的网站（见 gefei 路由下的竞品与收入侦察卡）。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 jinjiejiaocheng/08-zailiao-wajue-xuqiu-fangfa.md（原文发布 2024-08-13）

### 补充（来源：公开流传的哥飞群聊截图 2026-10-04 / 2026-10-22，2026-10-27 整理）
- **新词机会的量级**：谷歌官方口径是每年 5 万亿次搜索，其中每天有 15% 的搜索是全新的。他保守按其中 10% 是全新关键词来算：50000 亿 × 0.15 × 0.1 = 750 亿次每年，约合每天 2 亿次新词搜索。社群从 2023 年 11 月起，每个月的新词新站比赛都有网站拿到流量，他用这一点反驳"新词新站不长久"的说法。来源：公开流传的哥飞群聊截图 2026-10-22
- **ChatGPT 同样需要新词**："ChatGPT 也一样需要回答最新的问题，于是我们同样去做新词新站。"来源：公开流传的哥飞群聊截图 2026-10-04


## A1 — 原文中的应用 (Past Application)

### 案例 1：小工具站上线四个多月（20250825）
- **方法论的使用**：趋势里原词已下滑，对比找到一个热度稳中有升的相关词（不算新词），intitle 供应仅 3440、月搜索 20 万、KD 7。
- **结果**：4/7 注册域名、4/10 上线，GSC 28 天点击从 10 涨到 1500。

### 案例 2：GPTsHunter（20231111）
- OpenAI DevDay 刚结束就注册域名做 GPTs 导航，一天上线单页静态站，4 天获得 33 个引用域名。新事物出现 → 词根（Hunter/Store/导航）组合 → 抢速度。

### 案例 3：共识反例（20250421）
- 自己造的品牌名没人搜；吉卜力风格（Ghibli）爆火时，大家用的表达才有量——要跟随用户的说法而不是自己命名。

## A2 — 触发场景 (Future Trigger) ★

1. "不知道做什么站 / 找不到下一个关键词"
2. "怎么找新词 / 蓝海词 / 有需求的词"
3. "某个新模型/新游戏/新梗火了，能不能做站？从哪找相关词"
4. "怎么从竞品/同行那里发现机会"

### 语言信号
- "找词 / 挖需求 / 新词 / 热词 / 蓝海词 / 灵感 / 找关键词 / keyword research / 选题"

### 与相邻 skill 的区分
- 与 `gefei-keyword-evaluation`：本卡负责产出**候选清单**；"这个词值不值得做"的打分与结论交给判词卡。
- 与 `gefei-intent-site-structure`：本卡找主词；围绕主词收集全部长尾并规划页面在结构卡。

## E — 可执行步骤 (Execution)

1. **定方向与市场**：明确语言/国家（默认英语、美国/全球），以及可做的页面形态（工具/游戏/信息）。
2. **按渠道各取一批**（至少 3 个渠道）：趋势上升词、词根×新事物、同行 sitemap 新 URL、竞品付费词、站找站。
   - 完成标准：候选≥20 个，每个记录来源。
3. **趋势初筛**：对每个词在 Google Trends 拉 5 年和 12 个月；记录起始时间、走势（升/平/降）、季节性；与基准词（GPTs）对比相对热度。
   - 完成标准：剔除下滑中、纯季节性已过、热度近乎 0 的词。
4. **查共识**：同义表达在趋势里加引号对比，选大家实际用的说法；查词源（它是什么、谁在搜）。
5. **SERP 快看**：搜一下，看前排是不是大站首页、是否已被完美满足（细判交给判词卡）。
6. **输出候选表**：关键词 / 来源 / 出现时间 / 走势 / 相对 GPTs 热度 / 共识表达 / 初判（进入判词 or 放弃）。

## B — 边界 (Boundary)

- 新词红利随竞争者增多而缩短，作者 2026 年也说后发者半年到一年内仍可追上（靠外链/体验），先发优势不是护城河。
- Semrush/Similarweb 对新词数据滞后，量要以谷歌趋势/Ads 关键词规划师为准。
- IP/游戏名/品牌词有版权与仿冒风险（见 onpage 卡危险网站申诉）；本卡不评估法律问题。
- 谷歌趋势找新词方法已从GitHub 社群整理内容补上（见 I 节补充）；外链列表、内部找词工具、"8 种找词方式"原文仍缺，不要假装知道。
