---
name: gefei-onpage-launch
description: |
  当要写 Title/Description/H1、检查页面 SEO、选域名、部署上线（Cloudflare/Vercel/GA/GSC）、让谷歌收录、判断新站能不能批量上页面、或新站被 Chrome 提示危险网站时使用。上线后的索引/排名问题诊断用 gefei-gsc-diagnosis。
metadata:
  cangjie.generated-by: cangjie-tools v2.5.0
  cangjie.capability-id: cap.gefei.onpage-launch
  cangjie.capability-revision: 1
  cangjie.bundle-id: bundle.gefei
  cangjie.source-title: 「哥飞」公众号文章合集（2019–2026，862篇）
  cangjie.tags: 哥飞, 出海, SEO
---
<!-- capability_id: cap.gefei.onpage-launch | revision: 1 | status: active -->

# 站内 SEO 与上线收录清单（含新站放量节奏）

## R — 原文 (Reading)

> 总之一句话，服务好用户，让他只打开你一个网页就解决需求。那么谷歌就知道，你的网站跟这个搜索关键字很匹配，自然就会给你更好的排名。
>
> — 哥飞，《新网站上线最快多久能从谷歌获取搜索流量？》(20230904)

> 新站批量化上页面，必死。
>
> — 哥飞，《【哥飞SEO教程】新站批量化上页面,必死》(20250320，标题)

## I — 方法论骨架 (Interpretation)

**谷歌排名三段论**：页面的关键词信号（Title/H1/正文）让你进入候选 → 外链（含 nofollow）把你推进前 10 → 用户行为（停留、跳出、浏览页数）决定最终名次；谷歌会先给新页面一点测试流量。

**站内 SEO（TDH 取代 TDK）**：Keywords meta 已无用；Title、Description 每页唯一且含主词；一个 H1 含主词，H2–H6 层级清晰；工具页也要有说明文字；图片 alt；URL 含关键词；加载快、移动端友好；首页列出新内容；内链合理；原创、有信息量、持续更新；举全站之力做一个主题。

**上线链路**：域名（关键词.com → 带横杠.com → .net 等常见后缀，任意海外注册商）→ Cloudflare 解析 + HTTPS → GitHub + Vercel（或 Cloudflare Pages）部署 → GA/统计代码放在 `</body>` 前 → GSC 验证并提交 sitemap → 社区发帖/外链促收录。最小可上线站可以只是一个 HTML 页面，登录与支付不是上线前提。

**新站放量节奏**：判断是否"新站"（域名/上线 <6–12 月、引用域名 <100、DR<40、前 20 排名页面 <100）。新站先手工做精品页；10 个页面收录且有点击后加到 20 页，观察 GSC 再放量。

### 补充（来源：GitHub [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base)，2026-10-27 整理）
- **Title/Description 生成流程（哥飞，web.cafe 2024-07-29）**：不要直接让 GPT 写；先在 Similarweb/Semrush 关键词工具导出"词组匹配+相关关键词"，合并去重、按搜索量降序取前 100 个（只留词）喂给 GPT；多轮迭代并自己改写后让 GPT 润色；Title 一般 <60 字符，核心词突出，可在开头放吸引词（如 "AI"），带上次核心词，品牌名放最后；不用普通人不会搜的专业词，从关键词列表里换词。示例：`AI Chinese Names Generator & Meaning Explainer | ChinsesNames.ai`。Description 在 Title 定稿后生成，检查是否漏了核心词。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 xinshourumen/02-如何用GPT生成SEO友好的网页Title和Description.md
- **上线后收录与出词时间线（哥飞小课堂 2025-01-20）**：文案没问题一般 24 小时内收录；提交到谷歌爬虫常来的网站并配合外链，最快约 2 小时收录；收录后 24–48 小时 GSC 应有曝光。48 小时无动静按序排查：内容长度不够、关键词分布不合理、TDH 没覆盖关键词、核心词密度不够、页面为前端渲染。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 other/01-shangzhan-zhihou-yaozuoshenme.md
- **落地页版本（哥飞小课堂 2025-04-08）**：V1.0 = 工具页 + 博客；V1.5 = 工具页 + 落地页 + 博客；V2.0（社群现用）= 精品工具页面 = 工具功能 + 落地页图文 + 工具生成结果列表。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 other/02-gongju-luodiye-sheji.md

### 补充·第二批（来源：GitHub [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base)，小课堂与案例拆解，2026-10-27 整理）
- **获取 Bing 流量（哥飞群分享 2025-01-25，2025-03 回顾时每天两三百点击）**：① 提交到 Bing 站长后台；② 加 Sitemap；③ 按后台扫描结果逐项修复（缺 Description、缺 H1、Title 过长）；④ 支持并主动提交 IndexNow；⑤ 在 Cloudflare 开启主动推送。他的推测是：谷歌爬虫够强，不依赖 Sitemap；Bing 和国内搜索引擎为了省钱，更依赖站长提交。还有群友补充：开启 Cloudflare 的 Crawler Hints 也有效。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 jinjiejiaocheng/09-ruhe-huoqu-bing-liuliang.md、同仓库路径 judgeKey/34-wy1907a4n0.md
- **收录快慢**：一看内链做得好不好，二看有没有初始外链，"一两个就可以"。买老域名前，先上 archive.org 查有没有被用过，用过就换一个。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/19-m7wq53ovv4.md
- **改版不丢流量（案例 therighthairstyles.com）**：可以加新页面，但旧页面的 URL 和内容要保持不变。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/45-qxza0rekyl.md
- **爬虫预算（小课堂 2025-02-26）**：谷歌给每个站分配的抓取预算不同。大量低质页面会让预算被调低，已收录的页面也可能被移出索引；如果继续生产，就会受到惩罚。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/46-mdkswtcdsx.md

## A1 — 原文中的应用 (Past Application)

### 案例 1：48 小时出流量（20230904）
- 7/20 注册域名，7/21 GSC 已有谷歌点击：新词 + 关键词域名 + 满足意图 + 小词。

### 案例 2：小工具站（20250825）
- 上线前做好 On-Page SEO（元标签、谷歌喜欢的页面特征），所以 KD 低的词上线即有曝光点击。

### 案例 3：新站被提示"危险网站"（20261025）
- 域名与已收录老站相似 + 模板残留别家品牌 → 被判"欺骗性网页"；改掉品牌残留后在 GSC"安全问题"申请审核，说明做什么、改了什么、为何不是仿冒。

## A2 — 触发场景 (Future Trigger) ★

1. "页面 SEO 怎么做 / Title、H1、Description 怎么写？"
2. "网站做好了，怎么上线并让谷歌收录？"
3. "域名怎么选？要不要 .com / 带横杠？"
4. "新站能不能一次上几百个页面？"
5. "新站打开提示危险网站怎么办？"

### 语言信号
- "TDK / TDH / 元标签 / on-page / 上线 / 部署 / Vercel / Cloudflare / GSC 提交 / 收录 / sitemap / 域名 / 危险网站"

### 与相邻 skill 的区分
- 与 `gefei-intent-site-structure`：结构卡决定有哪些页面；本卡把每个页面做到可排名并上线。
- 与 `gefei-gsc-diagnosis`：上线后看信号、排名下滑 → GSC 卡。
- 外链怎么做 → 路由入口 `gefei`（backlinks-promotion 卡）。

## E — 可执行步骤 (Execution)

1. **域名**：按 关键词.com → 带横杠 → 其他常见后缀 选；先搜有无同名/近似老站（避免撞名）。
2. **逐页 TDH 检查**：唯一 Title（主词靠前）、Description（含主词与卖点）、唯一 H1、H2 覆盖长尾、alt、URL。完成标准：每页一张 TDH 表。
3. **体验检查**：首屏即满足意图（工具可直接用、免登录试用优先）、移动端、速度（Lighthouse/PageSpeed）、说明文字、FAQ、内链到相关页、品牌名清晰（不残留模板品牌）。
4. **部署**：Cloudflare DNS+HTTPS → Vercel/Pages → 统计代码 → robots.txt 与 sitemap.xml。
5. **提交收录**：GSC 验证、提交 sitemap、首页 URL 检查请求编入索引；社区发帖/目录提交拿首批链接。
6. **放量判断**：按"新站"四条标准判断；新站 10 页→20 页逐步加，每批看 GSC 收录与曝光。
7. **输出**：上线检查清单（逐项 ✅/❌ + 待办）。

## B — 边界 (Boundary)

- "停留时间/跳出率影响排名"是作者经验判断，谷歌未官方确认。
- TDH：Title/Description 生成流程已从GitHub 社群整理内容补上（见 I 节补充）；H 标签细则和新站页面细节仍未找到原文。
- 平台（Vercel/Cloudflare）计费与功能会变，执行时以官网为准。
- 中国大陆注册商/备案不在本卡范围（作者建议用海外注册商）。
