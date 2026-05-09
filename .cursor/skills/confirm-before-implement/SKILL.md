---
name: confirm-before-implement
description: >-
  Enforces alignment before coding: after Figma input, ask before adding any
  copy, assets, or features not in the file. Before any work involving
  backend logic, state the full flow (all branches, data sources, fallbacks),
  wait for agreement—never add unrequested alternative paths. Use for Figma,
  APIs, or ambiguous features. Invoke via @confirm-before-implement or 先确认再开发.
---

# Confirm Before Implement（先对齐再开发）

User expects **no silent implementation** and **no scope creep** beyond what was agreed.

## When this applies

- **Figma**：链接、node-id、截图、「按稿更新」。
- **含后端逻辑的功能**：HTTP/RPC/数据库/消息队列/定时任务/Serverless/CLI 调用服务端、Webhook、鉴权与存储等；凡**不在纯前端静态展示**、且存在**多路径、多数据源、降级、重试、缓存**等设计空间的，都按 Step 2 走。
- **任何**「做法不止一种」或「容易偷偷多加一层」的任务。

若用户写明「直接实现 / 无需确认」，可简述依据后动手。

---

## Step 1 — Figma / 设计稿：先确认，**不要直接实现**

在拉 MCP、改样式、下资源、写代码之前：

1. **复述**稿内范围（版面、交互、已有文案与图层）。
2. **禁止自作主张**：不要在未询问的情况下**新增或删减**「稿里没有明确要求」的**文案、图片、图标、模块或功能点**。若你认为有帮助，先 **提问：是否需要**，得到肯定答复后再做。
3. **列出待确认项**，例如：交互是否与既有约定一致、整图 vs HTML、资源命名与路径、断点策略等。
4. **等待用户回复**后再进入 Step 2 与编码。

---

## Step 2 — 开发前：说明**完整实现逻辑**，再写代码（**凡涉后端逻辑均适用**）

在用户确认 Step 1（及必要的业务意图）之后、提交 diff 之前，写清打算怎么做：

| 维度 | 说明要点 |
|------|----------|
| **目标** | 交付范围（接口契约、用户路径、持久化与否）。 |
| **数据来源与去向** | 调哪个服务、读哪张表、写哪里、是否异步。 |
| **处理时机** | 同步请求内 / 队列 / 定时 / 事件触发。 |
| **全部分支** | 含 **备选策略、降级、额外数据源、fallback、重试语义**；**禁止在未事先说明的情况下新增任何一种**。 |
| **风险与边界** | 幂等、一致性、权限、配额、失败暴露方式。 |

### 后端逻辑：禁止私自加「备选路径」

**不限定于某一类产品（音乐推荐等仅作历史示例）。** 只要涉及后端逻辑：**凡存在第二种实现方式**（另一接口、另一查询策略、另一缓存层、默默兜底的数据源等），都必须先在方案里**逐项列出是否会写进代码、默认是否启用**，由用户确认后再实现。

**不得**在未披露的情况下，为方便开发或自作聪明而**叠加备选逻辑、额外降级链路或与需求无关的第二条数据来源**。

用户点头后再实现与提交。

---

## Response shape（建议回复结构）

1. **Open questions**（含：稿外是否要加文案/图/功能）— 编号列表，必要时停在提问处。
2. **Proposed implementation** — **凡涉后端须附分支/数据源一览**；无隐藏 fallback。
3. **Implementation** — 确认后再写代码与变更说明。

---

## Checklist（自用）

- [ ] 未擅自增加稿未要求的文案、图片或功能；需要的已问过。
- [ ] Step 1 待确认项已澄清。
- [ ] Step 2 已说明逻辑；**凡涉后端已列出全部路径与数据源并得到同意**，未私自加备选逻辑。
- [ ] 仅在此之后：下载资源、改文件、跑命令。
