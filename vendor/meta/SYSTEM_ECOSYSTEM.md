---
origin_repo: tianxin-68/meta
origin_path: ecosystem/SYSTEM_ECOSYSTEM.md
origin_commit: 292f35cb2648e93dace423516375bc064c37ff0c
projection_scope: invest local vendored copy
runtime_dependency_on_origin: false
local_overrides: none
---

# System Ecosystem｜Invest Local Copy

> 跨项目关系的 Definition Authority 在 `meta/ecosystem/SYSTEM_ECOSYSTEM.md`；本文件用于 `invest` 独立运行。

```text
meta
= Method Source
        ↓
tx / Personal
= Owner Context Source
        ↓
   ┌────┴────┐
   ↓         ↓
  dw       invest
Career    Investment
Domain    Domain
```

## invest 的上游

```text
meta
→ Framework / Decision / Validation Method

tx / Personal
→ Objective / Values / Risk Preference / Behavior / Life Constraints
```

## invest 的定义权

`invest` 只拥有：

```text
Investment Domain Truth
Business / Industry Analysis
Valuation / Expected Return
Portfolio / Risk
Company Thesis
Investment Decision / Review
```

它不拥有：

```text
通用认知方法         → meta
通用 Human Mechanism → tx
Career Truth          → dw
```

## 决策关系

```text
Investment Decision
= Investment Domain Judgment × Personal Suitability
```

Personal 负责“什么适合 Owner”；Invest 负责“这个资产 / 行业 / 组合本身怎样”。

## Human Mechanism Projection

```text
Personal Human Source
→ Copy + Localize
→ Investor Behavior Rule
→ Trigger / Slow Path / Discipline
→ Decision Trace
```

本地可以增加投资场景特有规则，但不能重新定义通用 Human Mechanism。

## Physical Independence

```text
Canonical Source
→ copy / adapt
→ vendor/<origin>/...
→ Local Runtime
```

本仓运行不依赖 `meta` 在线存在；上游路径与 commit 只用于 provenance 和未来显式升级。

## Feedback

```text
Investment Reality
→ Review
→ Investment Source Correction

若反复暴露 Owner 风险承受 / 行为 / 目标偏差
→ Personal Correction Candidate

若多个 Domain 都暴露同一认知方法缺口
→ Meta Correction Candidate
```

## 一句话

> **Meta 教怎么想，Personal 定义 Owner，Invest 定义资本世界里的判断与决策。**
