# 学员内容：gangbo/gefei-make-money 2026-11 增量蒸馏

> **【学员内容】非哥飞原话。** 来源仓库 [gangbo/gefei-make-money](https://github.com/gangbo/gefei-make-money)。本轮处理到 commit `4a9859f52cfb1162997e4d96dc68f002cac2e553`（提交时间 2026-11-13 14:30，北京时间）。引用时必须标注「学员内容」，不得混作哥飞原话；与哥飞冲突时以哥飞为准。
>
> 数据时效：在线人数、票数、星数、搜索量等数字都是当时快照，下结论前须重查。

## 1. 网页休闲小游戏热度调研（研究日 2026-11-12）

来源：`research/notes/trending-web-casual-games-2026-11-12.md`（commit `4a9859f`，2026-11-13）。作者声明：只写亲自打开并核对过的页面事实，未稳定读到的 Trends / Semrush / 精确访问量不编造。

**可复用的调研方法**

- 门户要分开看，不要混成一张总榜：Poki 首页 live / Popular、CrazyGames 首页与 Hot（站点自称是近 24 小时升温，不是历史总票榜）、StatKraken 累计票、WebGameSpy 同时在线约数（站点写明是档位，不是精确 DAU）、itch.io 网页区「新且热门 / 最高分」。
- Similarweb 若只看到排名和停留、看不到访问总量，就不要写访问量；搜索摘要里互相矛盾的数字一律不用。
- 「AI 仿做难度」是给独立开发者的主观判断，不是来源数据。

**2026-11-12 快照（须重查）**

- Poki 首页当时「当前播放最多」前五：Level Devil、Smash Karts、Subway Surfers、Blocky Blast Puzzle、Drive Mad。
- WebGameSpy 当时估算 Poki 全站同时在线约 20.5 万；前列约数档包括 MineFun.io ≈ 1 万，Subway Surfers ≈ 5 千。
- itch.io 网页区当时以视觉小说、恐怖、互动叙事高分为主，和 Poki / CrazyGames 的超休闲门户不是同一套市场。

**给独立开发者的 5 条机会判断（学员结论）**

1. 优先「两键或一键、秒重开、十几秒内能感到核心乐趣」的轻量体验（如 Drive Mad、Stickman Hook、Space Waves、Slice Master、Level Devil 这类模式）。网页玩家用几秒而不是 30 分钟决定去留。
2. 单指解压（拖放消除、步骤式装修 / ASMR）仍有大流量，但已经拥挤；机会更多在手感、主题包装或更轻的体积，不要指望蓝海。
3. 「新钩子 + 门户推荐」可以几天内拉起来（当时举例：Country Balls World War 上线数日即进入 Trending，TNT Sandbox 一个月票数明显上涨）。清晰的梗或直觉反馈比大制作更能打。
4. 不要把「现在在线最高」当成仿做清单。MineFun.io、Bloxd.io、Smash Karts、Subway Surfers 靠多人基础设施或大 IP；可学「立刻能玩、可开私房、模式轮换」，不要复刻方块 MMO。
5. 分发是三个不同市场：Poki / CrazyGames（及 Coolmath）是免费网页门户，广告和平台分成是主流，适合轻量 HTML5；YouTube Playables 超休闲增量可能很大，但是 YouTube 渠道；itch.io 网页区更匹配故事向，不要指望它带来门户那种同时在线。热门品类本身不能自动解决变现问题。

## 2. 游戏开发 AI Skill / MCP（研究日 2026-11-10）

来源：`research/notes/game-dev-ai-skills-2026-11-10.md`（commit `4a9859f`，2026-11-13）。面向用 Cursor / Claude Code 做休闲 2D/2.5D、引擎候选 Godot / Unity / Cocos Creator、发布目标含微信 / 抖音小游戏的个人开发者。星数与 `pushed_at` 来自当时 GitHub API，须重查。

**学员结论（按目标，不是按星数）**

- 先装技能包，再按选定引擎加一个编辑器 MCP：技能包装怎么写脚本和手感，MCP 让助手能改场景、跑游戏，两者互补。
- 当时推荐起点：[Awesome Gamedev Agent Skills](https://github.com/gamedev-skills/awesome-gamedev-agent-skills)（同一套可用于 Cursor 和 Claude Code；含 game-feel、game-ui-ux、create-game-assets 等）。画面手感不必另找一个独立「juice」仓库。
- 引擎 MCP：Godot 优先当时维护更活跃的 [Godot AI](https://github.com/hi-godot/godot-ai)（要求 Godot 4.7+）；Unity 优先官方 [Unity-Technologies/skills](https://github.com/Unity-Technologies/skills)，再加 [MCP for Unity](https://github.com/CoplayDev/unity-mcp)。
- 若首发微信 / 抖音：主流跨引擎包当时不含 Cocos，需另补 [Cocos Creator Skill](https://github.com/hsiaozzz/cocos-creator-skill) 和 [cocos-mcp-server](https://github.com/DaxianLee/cocos-mcp-server)，并自行核实小游戏导出和广告 SDK。
- 不要一上来就装当时星数很高的 [Claude Code Game Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)：它主要为 Claude Code 设计，当时 README 主路径是浏览器原型，不一定最贴合 Cursor + 国内小游戏。也不要一上来全量安装多个代理，以免抢上下文。
- 像素图可试用 [SpriteCook skills](https://github.com/SpriteCook/skills)，但免费档额度有限，先小规模试验再考虑付费。

## 3. Ren'Py 网页体积、嵌入与传播（研究日 2026-11-11）

来源：`research/notes/renpy-visual-novel-notes-2026-11-11.md`（commit `4a9859f`，2026-11-13）。体积数字来自作者本地网页构建实测，不是官方基准。本文不收录任何具体作品内容或二进制。

- Ren'Py 可导出网页版，也可打安卓 / iOS 工程；**不能**直接做微信或抖音小游戏（这两类平台要 JavaScript / TypeScript 方案）。
- 网页体积有硬地板：一次未优化构建原始约 44MB；开启服务器 gzip/Brotli 后，`renpy.wasm` + `renpy.data` 合计约 11MB，很难再往下压。游戏内容在 `game.zip` 里，再 gzip 几乎压不动。一次精简后的恋爱向网页 demo，gzip 传输量约 16MB。若目标是首次加载 1–3MB 的网页小游戏，应改用纯网页方案。
- 优化三步：服务器压缩（确认 `.wasm` / `.data` 也被压）、精简 `game.zip` 里用不上的字体、压缩加载图。这三步降的是传输量和内容包，打不破约 11MB 的引擎地板。
- 嵌入：不要把运行时直接挂进主站的一个 `div`（容易接管页面和全局变量）。优先把游戏放到主站同源路径（如 `/games/xxx/`）再 iframe，或做成独立全屏游戏页。避免只放在子域再硬嵌进主站（跨源时容易白屏；若必须跨子域，需配好跨域隔离和 CORP 等响应头）。iframe 若加了 `sandbox` 却没有 `allow-same-origin`，IndexedDB 存档会失败。排查可看 `crossOriginIsolated`、`SharedArrayBuffer is not defined`、CORP 报错，并确认 `.wasm` 的 `Content-Type` 为 `application/wasm`。
- 口型开合不必严格对口型：闭嘴 / 张嘴图层加说话回调即可；只需部分台词配音时，给对应句加上 `voice`。严格跟声音对口型需要 Live2D，成本高得多。
- 传播结构可参考、不能推导成「用 Ren'Py 就会有流量」：鲜明好模仿的角色、一个能截图分享的点、短流程适合录视频。题材和商店政策要按自己的发布平台单独判断。

## 4. 商机筛选：Agent 替代测试（研究日 2026-11-08）

来源：`research/notes/opportunities-rescreen-2026-11-08.md`（commit `07e5cbc`，2026-11-11）。只收方法，不收该学员个人项目的否决清单或已上线产品。

- 先问：用户把任务交给 AI Agent 是否就能完成？若可以，不宜再当作独立站机会。
- 还要避免把「目录里有同类工具」当成需求证据：那只证明供给。
- 核心提醒：**抗聊天替代 ≠ 市场有空缺 ≠ SEO 能打得进。** 交互形态通过之后，仍要过免费竞品是否已经够用、词的搜索量与 KD、SERP 是否打得进。没有量级数据时，不要把「搜索结果数量」当成搜索量。
- 作者当时按此标准重筛后，没有宣布找到可立即立项的新商机；该项结论只对应当时候选，不是通用禁令。

## 本轮未收进本文的文件

- 该仓库中与本包已有方法大量重叠的需求挖掘综合笔记，本轮不整篇并入。
- `CURRENT-DECISIONS.md` 以及选品短名单、Semrush 批次表、方向批处理原文：属于该学员个人项目决策和过期词表，不收。
