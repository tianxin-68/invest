# Investment Cognitive & Decision System

> 角色：Owner 的 **Investment Cognitive & Decision System｜投资认知与决策系统**。
>
> 第一阶段目标不是追求短期收益，而是建立可验证、可复用、能控制永久性资本损失风险的投资认知与决策能力，并逐步提高资本配置质量与长期被动收入能力。

## 1. 系统定位

```text
Company / Industry Reality
→ Business Analysis
→ Investment Thesis
→ Valuation / Expected Return
→ Risk / Position Decision
→ Action / No Action
→ Result
→ Review
→ Source Correction
```

行为侧：

```text
Personal Human Mechanism
→ Investor Behavior Projection
→ Trigger / Slow Path / Discipline
→ Decision Trace
→ Reality Feedback
```

## 2. 当前核心入口

| 问题 | 入口 |
|---|---|
| `invest` 自身对象、职责、定义权与演进边界 | [`SYSTEM_ARCHITECTURE.md`](SYSTEM_ARCHITECTURE.md) |
| `meta / tx / dw / invest` 的关系与上游依赖 | [`vendor/meta/SYSTEM_ECOSYSTEM.md`](vendor/meta/SYSTEM_ECOSYSTEM.md)（vendored local copy） |
| AI 权限、写入规则与 Owner Gate | [`AGENTS.md`](AGENTS.md) |
| 真实投资决策记录模板 | [`templates/investment_decision.md`](templates/investment_decision.md) |

## 3. 当前五个 Concern

```text
Investor Behavior
Business / Industry Analysis
Valuation / Expected Return
Portfolio / Risk
Decision Trace / Review
```

不要为了目录完整提前建立宏观、量化、技术分析、期权等一级模块；只有真实重复问题证明现有结构无法承载时再新增。

## 4. Upstream Dependency

```text
meta
→ 怎么建模 / 决策 / 验证

tx / Personal
→ Owner 的目标、价值、风险承受、行为模式与人生约束

invest
→ Investment Domain Truth + Decision + Feedback
```

因此：

```text
Investment Decision
= Investment Domain Judgment × Personal Suitability
```

通用 Human Mechanism 归 `tx`；`invest` 只保存投资场景中的触发、纪律和决策 Projection。

跨项目关系的 Canonical Source 在：

```text
tianxin-68/meta@dev/ecosystem/SYSTEM_ECOSYSTEM.md
```

本仓通过 `vendor/meta/` 保存自包含副本，`runtime_dependency_on_origin = false`。

## 5. 后续目录按需生长

有真实资产时再创建：

```text
0_investor/
1_business/
2_valuation/
3_portfolio/
companies/
decisions/
reviews/
```

## 6. 一句话

> **先训练“判断—决策—复盘”闭环，不把 `invest` 做成股票收藏夹。**
