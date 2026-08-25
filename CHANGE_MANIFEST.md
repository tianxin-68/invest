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
