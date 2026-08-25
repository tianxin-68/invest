# Change Manifest｜Invest Local Projection

> 上游正本：`tianxin-68/meta@dev/ecosystem/CHANGE_MANIFEST_CONTRACT.md`。  
> 本文件只保留 Invest 本地执行投影，不取得跨项目 Definition Authority。

任何结构、语义、路由或治理改造必须：

```text
Before change
→ Proposed Change Manifest：改什么 + 为什么 + 影响 + 明确不改什么

Scope expands
→ Delta Manifest 后再扩大范围

After change
→ Actual Change Manifest：实际改动 + 缘由 + 验证 + commit
```

未进入清单的顺手清理、搬迁、改名、归档或语义调整默认禁止。投资真实买卖动作仍由既有 Owner Gate 单独约束，本规则只增加改造透明度，不改变资本配置权限。

---

## 2026-08-25｜Investment Coach

### Proposed Change Manifest

**改什么**

- 新增 `0_investor/investment_coach.md`，承载每周 2 次投资文章教练的训练契约与滚动沉淀；
- 在 `README.md` 的核心入口与训练循环中引用该入口；
- 自动化每次输出后，同步发送 Gmail，并将同一份内容追加到 `investment_coach.md`。

**为什么**

当前系统已经定义 Investor Formation 与周期训练，但文章输入、教练提炼、训练问题与长期沉淀之间还没有固定的运行入口。此次只把既有训练闭环落成可持续运行机制，不新增投资 Concern。

**影响范围**

```text
0_investor/investment_coach.md
README.md
Investment Coach automation
```

**明确不改**

- 不新增一级目录或新的投资 Framework；
- 不修改 `SYSTEM_ARCHITECTURE.md` 的 Concern / Definition Authority；
- 不把外部文章直接升级为 Investment Source；
- 不引入荐股、短线交易或真实仓位自动决策。

### Actual Change Manifest

**实际改动**

1. 新增 `0_investor/investment_coach.md`：定义每周 2 篇文章的 Selection Gate、Output Contract、Gmail/GitHub 双同步、Definition Authority 与 Stop Rule；
2. 更新 `README.md`：增加 Investment Coach 核心入口，并将其接入现有训练循环；
3. 更新既有 Investment Coach 自动化：每次生成后发送 Gmail `to: me`，并追加写入 `tianxin-68/invest@dev/0_investor/investment_coach.md`；
4. 保持 `SYSTEM_ARCHITECTURE.md`、`AGENTS.md` 与现有一级 Concern 不变。

**缘由**

把“每周阅读两篇”从单纯内容消费升级为可持续训练闭环，但不提前支付新的架构复杂度。

**验证**

- 已确认 `0_investor/investment_coach.md` 存在且包含 cadence、selection、output、Gmail、GitHub append 与 Evidence/Candidate 约束；
- 已确认 `README.md` 可从核心入口进入 Investment Coach，训练循环包含每周 2 篇；
- 自动化已更新为周二/周五运行，并包含 Gmail + GitHub 持久化动作。

**Repo commits**

```text
88eeba7  manifest: propose investment coach integration
1792f8b  investor: add investment coach training contract
93cb758  investor: wire investment coach into training loop
```

---

## 2026-08-25｜Resource Allocation Decision Projection

### Proposed Change Manifest

**改什么**

- 消费 `meta@dev/methods/resource-allocation-decision.md` 的通用资源配置决策方法；
- 新增 `0_investor/resource_allocation_decision.md`，形成 Investment Domain Projection；
- 将 `templates/investment_decision.md` 按真实决策执行顺序重排，并增加两层索引；
- 在 `README.md` 增加该 Source / Projection 的正式入口。

**为什么**

当前投资系统已有 Business、Industry、Valuation、Risk、Decision Trace 等局部 Source，但缺少一个低带宽的运行顺序来回答：在有限资本与风险约束下，应该比较什么、先判断什么、最后如何决定仓位。此次只建立跨 Concern 的执行编排，不新增一级 Concern。

**影响范围**

```text
0_investor/resource_allocation_decision.md
templates/investment_decision.md
README.md
```

**明确不改**

- 不修改 `SYSTEM_ARCHITECTURE.md` 的一级 Concern；
- 不改变真实 Buy / Sell / Add / Reduce 的 Owner Gate；
- 不把 Career Domain Truth 写入 invest；
- 不引入固定打分、机械权重或自动交易规则；
- 不顺手重构其他 Business / Valuation / Temperament Source。

### Actual Change Manifest

**实际改动**

1. `meta@dev` 新增 `methods/resource-allocation-decision.md`，把跨投资 / 职业重复出现的资源配置判断提炼为 Reasoning / Decision Meta Method；
2. `meta@dev/methods/README.md` 正式登记该 Method，并增加 Runtime 触发索引；
3. `invest@dev` 新增 `0_investor/resource_allocation_decision.md`，按 `A Frame → B Understand → C Price → D Protect → E Allocate` 做自包含本地 Projection；
4. `templates/investment_decision.md` 按 A0–E1 两层索引重排，仓位 / Action 延后到价值、价格、回报、风险与可逆性判断之后；
5. `README.md` 增加统一资源配置顺序入口与 Dependency 路径；
6. 保持 `SYSTEM_ARCHITECTURE.md`、Owner Gate 与一级 Concern 不变。

**缘由**

把“好公司 / 好行业 / 好岗位”与“是否值得配置稀缺资源”分开，形成一个跨域可复用、投资域可直接执行的决策顺序；减少从对象光环或趋势判断直接跳到高投入的错误。

**验证**

- 已读取验证 `meta@dev/methods/resource-allocation-decision.md`，包含 A0–E1 两层索引、Investment / Career Cross-domain Case 与 Decision Quality Standards；
- 已读取验证 `invest@dev/0_investor/resource_allocation_decision.md`，明确 `runtime_dependency_on_meta: false`，并保持 Projection 身份；
- 已读取验证 `templates/investment_decision.md`，执行顺序已对齐 A→E，且 `E0 Position / Action` 位于 Price / Return / Risk / Optionality 之后；
- `README.md` 已建立正式入口；
- 未修改 Invest / Meta 的 Frozen System Architecture。

**Commits**

```text
meta@dev
54df77a  decision: add resource allocation method
fcac843  meta: index resource allocation decision method

invest@dev
fa5c06c  manifest: propose resource allocation decision projection
b5fb570  investor: add resource allocation decision projection
99b18df  investor: reorder decision trace by runtime sequence
06b388c  investor: index resource allocation decision
```

---

## 2026-08-25｜Resource Allocation Framework Reclassification

### Proposed Change Manifest

**改什么**

- 保留 `0_investor/resource_allocation_decision.md` 的 A→E 投资决策链与 A0–E1 两层索引；
- 将其从“Meta Resource Allocation Method 的 Local Projection”重分类为 **Invest Domain Framework**；
- 移除错误的 Meta provenance / Projection 身份，避免一个尚未经 Local-first Promotion Gate 验证的抽象反向取得跨域定义权。

**为什么**

该框架首先是在投资问题中形成并用于真实消费的 Domain Framework。按新的 `Local Execute → Meta Candidate → Owner Gate → Meta Publish` 规则，应先让投资框架在本域运行和校准，再提炼真正跨域的构造 Learning；不能因为能类比 Career 就直接升格为 Meta Source。

**影响范围**

```text
0_investor/resource_allocation_decision.md
CHANGE_MANIFEST.md
```

**明确不改**

- 不删除 A→E 决策顺序与 A0–E1 索引；
- 不修改 `templates/investment_decision.md` 当前执行顺序；
- 不修改 Invest 一级 Architecture / Concern / Owner Gate；
- 不在本轮把“层级少、每层元素尽量少”直接写入 Meta Source；它保留为后续 Meta Candidate。
