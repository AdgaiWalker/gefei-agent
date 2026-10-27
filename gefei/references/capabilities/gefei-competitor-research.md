<!-- capability_id: cap.gefei.competitor-research | revision: 1 | status: active -->

# 竞品与收入侦察：一个网站赚不赚钱、靠什么拿流量、是谁做的

> 本卡完全来自 2026-10-27 第二批补充的社群小课堂和案例拆解，公众号正文中这部分内容较少。每条都注明了来源文件。

## R — 原文 (Reading)

> 假设他愿意花这么多钱买流量，说明买来的流量能够赚回来这么多钱，也就是至少不亏本。
>
> — 哥飞，小课堂 playhop.com 案例（2025-03-24），来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/49-1fhlbn26ii.md

> 用 ads.txt 文件，可以关联站长。
>
> — 哥飞，emojicombos.com 案例（2025-03-11），来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/48-9f589mpe04.md

## I — 方法论骨架 (Interpretation)

| 想知道 | 方法（哥飞的说法） | 来源 |
|---|---|---|
| 这个站有没有收钱 | 在 Similarweb 里看它的出站流量，有没有流向 Stripe 等支付域名（方法来自彪哥） | judgeKey/16-nz5kw1eht2.md |
| 大概赚多少钱 | Stripe 结账页访问量 ≈ 订单尝试次数；收入 ≈ 访问量 × 支付成功率（哥飞自己的 AI 工具站在 10%–50% 之间）× 客单价。没有自定义结账域名时，可以看 checkout.stripe.com 的来源站排行 | judgeKey/18-2noz8xxf2n.md、jinjiejiaocheng/05-paihangbang-wajue-zhuanqian.md |
| 收入排行榜 | Toolify 收入榜、IndieHackers 的 Stripe 认证榜、seo.box/referring（Stripe 入站排行） | jinjiejiaocheng/05、judgeKey/44-xlft7pezkb.md |
| 一个访问值多少钱 | 用它的投放花费 ÷ 买到的访问量，按"至少不亏本"反推。playhop 案例算出 PC 端每访问约 0.52 美元、移动端约 0.34 美元，再推算出自然搜索流量年收入约 2000 万美元 | judgeKey/49-1fhlbn26ii.md |
| 哪些词有人愿意付钱 | 看竞品付费投放的非品牌词；一直有人投广告的词，说明一直有人在赚钱 | judgeKey/16、jinjiejiaocheng/08 |
| 网站背后是谁 | 对比 /ads.txt 里的谷歌发布商 ID，加上站与站之间的互链 | judgeKey/48、judgeKey/12-oeohjryji6.md |
| 网站的历史 | 用 archive.org 的 CDX API 拉快照列表，判断是老站转型还是买了老域名，以及改版时是否保留了原来的 URL | judgeKey/45-qxza0rekyl.md |
| App 类收入参考 | Sensor Tower（案例：怀孕类 App 月收入约 900 万美元） | judgeKey/21-u1i1ol4m4v.md |
| 流量从哪来 | Similarweb 的渠道分布、Ahrefs 和 Semrush 的流量曲线及页面流量。注意两家的反链计数标准不同，数字对不上是正常的 | judgeKey/49、judgeKey/46-mdkswtcdsx.md |

## A1 — 原文中的应用 (Past Application)

### 案例 1：playhop.com（2025-03-24）
- 渠道构成：直接访问 30%、自然搜索 35%、付费 30%。按 0.52 / 0.34 美元每访问估算，年收入约 5364 万美元，其中广告投放花费约 1400 万美元。来源：judgeKey/49-1fhlbn26ii.md

### 案例 2：emojicombos / lingojam / perchance
- 三个站 ads.txt 里的发布商 ID 相同，站之间互相给链接，可以判断是同一个站长。来源：judgeKey/48-9f589mpe04.md

### 案例 3：therighthairstyles.com
- 2013 年的域名，2024 年首页加上了 AI 发型工具。从 archive.org 快照看，几次改版都保留了原来的 URL，所以 SEO 流量没有丢。来源：judgeKey/45-qxza0rekyl.md

### 案例 4：感谢信站时间线（2024-12）
- 原站站长 2023 年 3 月接受了 Starter Story 采访，同年 12 月就有模仿者注册域名上站（哥飞"合理怀疑"两者有关）。来源：judgeKey/30-t5g81oxxce.md

## A2 — 触发场景 (Future Trigger)

1. "这个网站赚多少钱？靠什么赚？"
2. "这几个站是不是同一个人做的？"
3. "这个关键词有没有人愿意付钱？"
4. "这个老域名或老站以前是做什么的？"

### 语言信号
- "收入估算 / Stripe / 出站流量 / ads.txt / 发布商 ID / archive.org / 竞品分析 / 流量价值 / 投放反推"

### 与相邻卡的区分
- 判断某个词能不能做，用 `gefei-keyword-evaluation`；本卡只负责看清竞品。
- 给自己的站定价、算账，用 `gefei-monetization-pricing`。

## E — 可执行步骤 (Execution)

1. 列出目标站，用 Similarweb 记录：总访问量、渠道分布、出站域名（找 Stripe、Paddle 等支付域名）。
2. 如果有支付出站：按"结账页访问 × 成功率区间（10%–50%）× 客单价"给出收入区间，不给单点数字。
3. 如果有付费流量：用投放花费 ÷ 访问量估出每访问价值，再乘以自然搜索流量。
4. 拉取 /ads.txt 和站间互链，判断背后是谁、是否在做站群或饱和式建站。
5. 用 archive.org CDX 查看域名历史和改版记录。
6. 输出一张侦察表（站点 / 访问 / 渠道 / 收入区间 / 证据链接 / 置信度）。

## B — 边界 (Boundary)

- 以上都是第三方估算加"至少不亏本"的假设，只能给数量级，不能当作真实财务数据。
- Similarweb 在 2025-07 之后部分页面数据已经取消（见 jinjiejiaocheng/08），工具能看到什么以当前实际为准。
- 只研究公开数据，不碰非公开数据，也不做仿冒。
