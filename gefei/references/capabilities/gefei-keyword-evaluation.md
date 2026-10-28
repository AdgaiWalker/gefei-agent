<!-- capability_id: cap.gefei.keyword-evaluation | revision: 1 | status: active -->

# 判断一个关键词值不值得做：量 × 供应 × 强度 × 回报

> **数据时效规则（2026-10-28 加，采纳 X 用户 @growaiskills 的反馈）**：本卡的方法可以复用，但引用原文里的搜索量、KD/竞争、CPC、价格、收入、外链数等都是**当时的历史数据**，出处旁已标原文发布日期。下结论前要按当前重查：近期搜索量（Google Trends / Ads 关键词规划师）、当前搜索结果页前 10、当前竞品价格；必要时注明适用条件（时间、市场/语种、站点类型）。数据对不上时，以重查结果为准，方法不变。

## R — 原文 (Reading)

> 你如果做一个新网站，想要进入谷歌搜索“uuid generator”或者“uuid online”的前10，需要你的网站至少有71个外部网站链接……投入产出比这么低，为什么不换另一个词去做另一个网站呢？
>
> — 哥飞，《用一个真实例子教你如何判断一个关键词是否值得做网站》(20231219)

> 每个关键词，你都看看谁会买这个关键词带来的流量，如果没有潜在买家，那么CPC就没有参考意义。
>
> — 哥飞，《看关键词挖掘需求时，CPC到底有没有参考价值？》(20250427)

## I — 方法论骨架 (Interpretation)

每个关键词的搜索结果都是一个**排行榜**；判词就是回答"榜上有多少人、有多强、我挤进去值不值"。四个维度缺一不可：

1. **量（需求）**：谷歌 Ads 关键词规划师/趋势为准（第三方工具对新词滞后）；与基准词（如 GPTs）对比；趋势方向比绝对值重要。
2. **供应（多少页面在竞争）**：intitle/allintitle 结果数；**KGR = intitle 结果数 ÷ 月搜索量**，<0.25 好机会，0.25–1 可考虑，>1 难。
3. **强度（前排有多强）**：Ahrefs KD 及"进前 10 需要多少引用域名"；打开真实 SERP 看前 10 是**首页还是内页**（自己首页可以打别人内页）、是大站还是新站、内容是否满足意图。KD 高但前排是大站内页、内容不对题 → 可做；KD 低但前排是 time.com 这类大站首页 → 陷阱。
4. **回报**：能否变现（工具付费/广告）；CPC 只对靠广告的内容站有意义，工具站看"谁会为这类用户付钱"；用倒推（排名 CTR × 搜索量 × UV 价值）估月收入，对比所需外链成本。

早期公式 **kdroi = 搜索量 × CPC ÷ KD**（2023）可用于批量排序，但作者 2025 年起"看关键词一般不看 CPC"，只作参考。

### 补充（来源：GitHub [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base)，2026-10-27 整理）
- **KD 与 KGR 怎么看（哥飞小课堂 2025-11-15）**：KGR 引入 intitle 数，衡量的是网页供应量，也就是竞争者的**数量**；KD 看前 20 名的外链、域名权重、页面权重以及首页还是内页，衡量的是竞争者的**质量**。两者不正相关，必须同时看。两者都低的词多半是新词，但新词可遇不可求，老词也要做。第三个维度应该是用户行为数据，但哥飞说量化公式"暂时还没结果"。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/10-hxx4rf13h1.md（原文发布 2025-12-01）
- **判词全流程（哥飞小课堂 2025-01-22）**：① 谷歌搜索看前 10 名里首页、内页各有几个；是首页就看整站流量，是内页就用 Similarweb 看这个内页的流量。② 用 Ahrefs 查 KD，以及前三名的流量和外链。③ 用"流量 ÷ 外链数"粗算投入产出。案例：aes encryption online 不值得单独注册域名建站，但已有站的内页可以做；stargate ai 这类公司名词不能建域名站（等于假冒官网）。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/02-87n8tt7m9r.md（原文发布 2025-10-11）
- **图片类词慎做（哥飞小课堂 2025-01-15）**：如果 SERP 先出 Images 模块，即便排第一，也只拿到约 6% 的曝光点击（sky background 案例：6.8K/109.9K）。这类词 Ahrefs 显示的低 KD 是算法局限；凡是谷歌在结果顶部直接给出答案的词（图片、视频、商品、计算公式）都要慎重。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/04-ixzzzz687q.md（原文发布 2025-01-15）
- **高 KD 新需求词**（哥飞 2025-01-20）：近一两年因 AI 才出现的新需求，KD 六七十也可以做，只要搜索量够大。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 other/01-shangzhan-zhihou-yaozuoshenme.md（原文发布 2025-01-20）

### 补充·第二批（来源：GitHub [hlwhut225/gefei-knowledge-base](https://github.com/hlwhut225/gefei-knowledge-base)，小课堂与案例拆解，2026-10-27 整理）
- **只和前 200 名比赛（小课堂 2025-01-20）**：能出词，说明页面已经进了这个词的前 200 名。判断一个词好不好做，看的就是这 200 个页面强不强。新词好做，是因为一开始参与排名的 200 个页面"大多数都是弱鸡"。先发优势只能维持到强对手入场为止。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/01-go8e119lew.md（原文发布 2025-10-11）
- **判词看五类数据（小课堂 2025-01-22 总结）**：① 关键词搜索量（谷歌趋势、Ads 关键词规划师、Similarweb）；② 搜索结果（谷歌、Ahrefs KD）；③ 网站流量（AITDK、Similarweb）；④ 单个网页的流量（Similarweb）；⑤ 外链（Ahrefs Backlink）。他的结论有两条：搜索量小、竞争又大的词完全不考虑；有一定搜索量的词，竞争大一些也可以做。ai face swap 案例里，判断"还能做"的依据是谷歌只给第一名出了 mini sitelinks。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/01-ruhe-panduan-guanjianci-shifou-nengzuo.md（原文发布 2025-01-22）
- **关键词是树状的，要"边收边扩"（案例 2025-12-05，paypal fee calculator）**：Calculator → Fee Calculator → PayPal Fee Calculator，越靠近主干竞争越激烈。删掉限定词是"收"，用谷歌下拉框和 Ahrefs/Semrush/Similarweb 查词是"扩"。定下主词后，再把它下级的细分词逐个做成页面，这就是"举全站之力"。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/09-3nfxk91lnj.md（原文发布 2025-12-09）
- **短期热点不追，找长期需求（小课堂 2025-11-17）**：NYT Connections 这类热词的热度不超过三天，社会新闻词也不适合单独建站。要找的是"今天、下个月、明年都有人搜"的需求。已经流行很久的游戏词，先用 KGR 看网页供应量。image to video ai 这种全球都看得到的新词，赶早上站也不保证一直领先，"追兵甚猛，不要躺平"。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/11-ot920u971o.md（原文发布 2025-12-01）
- **"大流量但 KD 为 0"往往是虚低（案例 2025-01-14，hdhub4u）**：这类词的搜索结果被 DMCA 频繁清掉，上榜的网站都很新，所以 KD 显示偏低。新域名不要按 KD 工具建议的外链数去估。另外，加不加双引号的热度对比，可以用来判断哪个说法才是主流表达（low taper fade 和 fade low）。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/45-qxza0rekyl.md（原文发布 2025-10-11）
- **估新词搜索量用参照词**：happy birthday images 全年稳定，日均约 5 万次；good morning images 日均约 13 万次。可以拿它们当比例尺，换算日搜索量在几万到十几万之间的词。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/21-u1i1ol4m4v.md（原文发布 2025-11-05）
- **用数据说话，不用经验（案例 2024-12-08，capitalizemytitle.com）**：在线字数统计、标题大小写转换这类"Word 里就有"的需求，照样有人大量搜索。新工具站最简单的路，是找老需求的新说法。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/28-08zfe1fbve.md（原文发布 2025-10-29）
- **信息增量（小课堂 2025-08-10，依据谷歌专利 US20200349181A1）**：老词的搜索结果已经被真实用户检验过，内容平平无奇的新页面很难排上去；新词还没有能满足需求的页面，所以写得一般也能拿到排名。工具站和游戏站额外提供服务，排名时谷歌还会参考用户行为数据。来源：https://github.com/hlwhut225/gefei-knowledge-base 路径 judgeKey/54-i33t7dyhxb.md（原文发布 2025-10-10）

### 补充（来源：公开流传的哥飞群聊截图 2026-10-04 / 2026-10-22，2026-10-27 整理）
- **商标风险会终结一个词的生命周期（Sprunki 案例）**：Sprunki 在 2024 年 5 月出现、9 月爆发，直到 2025 年 3 月还有新站能靠它拿到流量，在小游戏词里属于罕见的长寿词。但它后来被 incredibox 注册了商标，所以他说"现在不建议做了"。判词时要加查商标状态。截图在讲述商标之后的处理时被截断。来源：公开流传的哥飞群聊截图 2026-10-22


## A1 — 原文中的应用 (Past Application)

### 案例 1：UUID generator 不做（20231219）
- 收窄需求得到 "uuid generator/online"；Ahrefs 显示进前 10 需 71 个引用域名；趋势热度只有 GPTs 的一半到十分之一；前三网站月访问 43 万/3 万/13 万。
- **结论**：难度高、回报低 → 换词。

### 案例 2：老词也能做（20250825）
- 非新词，但 intitle 3440、月量 20 万、KD 7，KGR 与 EKGR 都低 → 做，四个月 28 天点击从 10 到 1500。

### 案例 3：KD 很高的词也能做（20260629）
- KD 反映前排强度，intitle 反映供应；前排多为不对题的内页时，新站用聚焦首页仍可上榜。

## A2 — 触发场景 (Future Trigger) ★

1. "这个关键词值不值得做 / 能不能做站？"（给出一个或几个词）
2. "KD 50 / CPC 很低 / 搜索量 1 万，能做吗？"
3. "几个候选词里选哪个先做？"
4. "KGR 怎么算 / intitle 怎么看？"

### 语言信号
- "值不值得做 / 能不能做 / 判断关键词 / 竞争度 / KD / KGR / CPC / 难度 / 排序"

### 与相邻 skill 的区分
- 与 `gefei-keyword-discovery`：那边产出候选，本卡打分下结论。
- 与 `gefei-gsc-diagnosis`：已上线的站为什么没排名 → GSC 卡；上线前评估 → 本卡。

## E — 可执行步骤 (Execution)

1. **收窄需求**：泛词用下拉/相关搜索收窄成可做的具体表达（如 uuid → uuid generator）。
2. **取量**：Ads 规划师月均搜索（选地区/语言）+ 趋势与 GPTs 对比 + 走势。完成标准：记录月量、趋势方向、季节性。
3. **取供应**：`intitle:"关键词"`（或 allintitle）结果数；计算 KGR。
4. **取强度**：Ahrefs KD 与所需引用域名；逐个看前 10：URL 类型（首页/内页）、站点类型（大站/新站/垃圾站）、是否满足意图、引用域名数（几百为好信号，低流量站却有 1K+ 引用域名 → 外链竞赛，避开）。
5. **算回报**：选变现方式→估目标排名 CTR（第 1 名约 20%+、第 3 名约 10%）→日 UV→月收入；对比外链与开发成本。
6. **下结论**：做 / 观察 / 不做，附 3 条理由；多个词时按（量×可达排名×UV价值）÷所需外链 排序。
7. **输出判词表**：关键词 / 月量 / 趋势 / intitle / KGR / KD / 所需引用域名 / 前10首页数 / 意图是否被满足 / 变现路径 / 估算月收入 / 结论。

## B — 边界 (Boundary)

- KGR 阈值来自外部长尾博客公式，哥飞将其扩展到新词，属经验工具；数据源（intitle 结果数）本身波动大。
- 第三方 KD/搜索量对新词严重滞后；不要只凭一个指标做决定。
- 收入估算中的 CTR、RPM、UV 价值都是经验默认值，因站、国家、品类差异大。
- 不评估版权/商标/合规风险；也不保证排名。
