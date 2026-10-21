# GitHub 主页装修 — 完整交接文档

> 账号：[shanananana](https://github.com/shanananana)  
> Profile 仓库：[shanananana/shanananana](https://github.com/shanananana/shanananana)  
> 文档路径（本地）：`/Users/shanananana/shanananana/docs/GITHUB-PROFILE-HANDOFF.md`  
> 文档路径（GitHub）：https://github.com/shanananana/shanananana/blob/main/docs/GITHUB-PROFILE-HANDOFF.md  
> 最后更新：2026-10-21

---

## 1. 目标与参考

| 项 | 说明 |
| --- | --- |
| **目标** | 把 GitHub 个人主页装修成「像活人」：个人介绍为主，不是产品说明书 / 技术栈展板 |
| **参考** | [yuchiXiong](https://github.com/yuchiXiong) — 借鉴排版（介绍 + 数据区），不要照抄玩梗强度 |
| **反面** | 早期版本：Focus 徽章、Webhook/API 堆砌、Demo 字样、capsule-render 慢动画顶图、整页技术营销腔 |

---

## 2. 本地与线上一致性

### 2.1 仓库与文件

| 文件 | 作用 |
| --- | --- |
| `README.md` | Profile 首页正文（GitHub 自动展示在主页顶部） |
| `assets/header.svg` | 顶图（静态 SVG，相对路径 `./assets/header.svg`） |
| `assets/footer.svg` | 页脚装饰条，**已从 README 移除引用**，文件仍在仓库，可删 |
| `docs/GITHUB-PROFILE-HANDOFF.md` | 本文档 |

**本地根目录：** `/Users/shanananana/shanananana/`

### 2.2 GitHub 账号状态（2026-10-21 查询）

| 字段 | 值 |
| --- | --- |
| 显示名 | shanananana |
| Bio | 空 |
| Location | Beijing |
| Company（Settings） | MOMO.Inc（**用户要求主页不要展示 Day Job / 公司标签**，Profile README 已无；Settings 里 company 字段未改） |
| Website | 空 |
| Pin | **仅 2 个**：`deepticket`、`ad_agent`（用户明确：两个就够） |
| 公开 repo 约 | 18 |

**Bio 建议稿（用户未在 Settings 确认）：**  
`自托管 Agent · 工单排障 · DeepTicket 作者 · 北京`  
或更生活向，需用户定稿。

**CLI 限制：** `gh api PATCH user` 改 Bio 需要 `gh auth refresh -h github.com -s user`。

---

## 3. 用户明确偏好（硬约束）

1. **Pin 只要 2 个**：deepticket、ad_agent。  
2. **不要 Demo 感**：项目描述、链接文案不要「示例 / Demo / 学习项目」当门面（ad_agent 仓库本体 README 可保留学习说明，Profile 层弱化）。  
3. **不要公司标签**：README 已去掉 MOMO / Day Job 徽章。  
4. **顶图**：不要慢动画（已弃用 capsule-render）；要静态、加载快。  
5. **个人介绍为主**：技术能力通过项目和数据区体现，首屏先是人。  
6. **朋友圈**：用户曾提供朋友圈截图作气质参考；**禁止把朋友圈原文、具体动态、地点人名抄上 README**。  
7. **语气**：用户多次反馈 AI 写的话「太二」——要正常口语、短句、少修辞、少段子、少 emoji，像本人打字。  
8. **已删除模块**：「其它仓库」表、views 计数（komarev）、底部宽 footer、`<details>` 折叠的 GitHub 数据（改为默认展开）。  
9. **GitHub 数据**：两卡并排，尽量同宽同高（当前 `card_width=430`，`width="49%"` `height="195"`）。

### 3.1 用户提供的真实人设（「关于我」事实源）

| 事实 | 内容 |
| --- | --- |
| 出生 | 1998（用户自嘲「上时代」） |
| 地域 | 北京 |
| 爱好标签 | 老二次元 |
| 音乐 | 喜欢毛不易的歌 |
| 运动 | 爱爬山 |
| 长期目标 | 三山五岳、五湖四海 |
| **进度** | **三山 1/3 · 五岳 4/5 · 五湖四海 0** |
| 工作方向 | 后端；Agent / 内部系统相关（DeepTicket 为自用后开源） |
| 爱好项目 | shanaTavern（和 KPI / 上班无关） |
| 联系 | Issue 可见会回（具体措辞需用户定稿） |

**当前 README「关于我」仍偏 AI 味，待重写示例（勿直接当终稿）：**  
含「给自己挖了个坑」「循环列表占比最高」「后头这项还没动过」等——用户不满意。

---

## 4. 当前 Profile 结构（README.md）

```
顶图 header.svg
## 关于我          ← 5 条 bullet，待改语气
## 最近在维护      ← 2 项目表格 + social star 徽章
## GitHub 数据     ← stats + top-langs 两图，默认展开
（结束，无 footer / views）
```

### 4.1 顶图文案（header.svg）

- 主标题：`shanananana`
- 副标题：`在北京做后端，开源一些自己在用的项目`
- 用户曾否决副标题：`北京 · 写代码，也好好过日子`（太二）

### 4.2 GitHub Stats URL（勿加 include_all_commits）

**Stats：**

```
https://github-readme-stats.vercel.app/api?username=shanananana&show_icons=true&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=8957e5&text_color=c9d1d9&card_width=430
```

**Top langs：**

```
https://github-readme-stats.vercel.app/api/top-langs/?username=shanananana&layout=compact&langs_count=6&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9&hide=html,css,scss,dockerfile&card_width=430
```

**已知问题：**

- 公共 Vercel 实例偶发限流/超时，Stats 可能空白，强刷或稍后重试。
- 曾用 `include_all_commits=true` → 报错 `Could not fetch total commits`。
- `github-readme-activity-graph.vercel.app`、`github-readme-streak-stats.demolab.com` 在用户侧曾裂图，**已移除**。

---

## 5. 账号与项目背景（公开信息摘要）

### 5.1 早期外部评价（聊天总结，供叙事用）

- 2018 注册；repo 比人红（deepticket ~71★，粉丝很少）。
- 能打原创：**DeepTicket**（AI 工单排障 / Agent 编排，Python、OpenHands、Docker、中英 README）、**ad_agent**（Spring AI 广告垂类）、**shanaTavern**（本地酒馆 FastAPI）。
- 问题：约一半公开库为 0★ fork；Bio 空；人设曾显得「严肃 AIOps」与「整活 fork」混杂。
- 建议叙事主线：DeepTicket + ad_agent；fork 不 pin、可 Archive。

### 5.2 原创 vs Fork（2026-10 快照）

**原创（非 fork，按 star）：**

| Stars | 仓库 | 说明 |
| ---: | --- | --- |
| 71 | deepticket | AI 工单排障工作台 |
| 25 | ad_agent | 广告垂类 Agent |
| 1 | spider | 爬虫（较老） |
| 0 | deepticket4java | DeepTicket Java 线 |
| 0 | spring-ai-markdown-skills | Spring AI Markdown 技能 |
| 0 | shanaTavern | 本地 AI 酒馆 |
| 0 | mcpDemo | MCP 备忘 |
| 0 | SystemCore | OS 学习 |

**Fork 示例（降噪候选，不 pin）：** JavaGuide、airi、MoneyPrinterTurbo、claude-code-haha、claw-code、fucking-algorithm、spring-framework 等。

**Profile 仓库「其它仓库」表已删**——若恢复，用户需确认是否列出 deepticket4java / shanaTavern 等。

### 5.3 与工作区关系

- 本机常见路径：`/Users/shanananana/deepticket/`、`deepticket-java/` 等；与 hello-agents 等无直接引用关系（除非后续用户要写进叙事）。

---

## 6. 装修时间线（commit 摘要）

| Commit | 说明 |
| --- | --- |
| 初始 | 创建 profile README，capsule-render 顶图 |
| 后续 | 去 MOMO 徽章；去 Demo 腔；静态 SVG 顶图；DeepTicket 风 dark banner → 改活人介绍 |
| 个人化 | 朋友圈气质抽象（未抄原文）；去 streak；改顶图副标题 |
| 布局 | 删其它仓库；GitHub 数据展开；两卡等宽；删 views + footer |
| `e808ad7` | 关于我写入 98/二次元/毛不易/爬山进度（语气待改） |
| `097dcaa` | 顶图副标题改为「在北京做后端，开源一些自己在用的项目」 |

完整历史：`git log --oneline` @ `/Users/shanananana/shanananana`

---

## 7. 待办（给接手人）

### 7.1 优先级高

- [ ] **重写 `README.md`「关于我」**：仅用 §3.1 事实，语气自然，用户审一遍再 push。
- [ ] **顶图副标题**是否与关于我一致，避免两套人设。
- [ ] 用户审阅后更新 **GitHub Settings → Bio / Website**（可选）。

### 7.2 优先级中

- [ ] 删除未使用的 `assets/footer.svg`（或恢复为极简底边，用户曾嫌「很宽」）。
- [ ] Stats 两卡高度视觉不齐时：调整 `layout=donut` 或 `langs_count` / `height`。
- [ ] 老 fork **Archive** 清单执行（用户未授权批量操作）。

### 7.3 优先级低 / 可选

- [ ] 顶图改用 DeepTicket `docs/assets/banner-header.png` 裁剪版（更品牌/二次元，用户未选）。
- [ ] Profile README 仓库设为 private？（一般 profile  repo 需 public 才展示。）
- [ ] 参考 yuchiXiong 增加 Wakatime / 博客 RSS（用户无站点则跳过）。

---

## 8. 附录：当前 README 全文快照

见仓库 `README.md`；修改前请 `git pull`。核心段落以 Git 为准，本文档不重复粘贴全文以免 stale。

---

## 9. 附录：顶图 SVG 要点

- 尺寸：1200×132  
- 深色渐变 + 轻 wave + 居中主副标题  
- 无动画、无外链图片依赖  

---

## 10. 给接手 AI / 协作者的一句话

**文件在 `/Users/shanananana/shanananana/`，结构和 Pin 已定；主要工作是用人话重写「关于我」和必要时微调顶图副标题，严格用用户给的 98/北京/老二次元/毛不易/爬山进度事实，禁止抄朋友圈、禁止 Demo/公司标签、禁止「太二」的 AI 腔。**
