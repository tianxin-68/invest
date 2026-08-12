# Investment Cognitive & Decision System｜System Architecture

> **唯一职责**：定义 `invest` 的系统对象、职责边界、定义权、决策闭环与演进门禁。

## 1. Objective

> **提高长期资本配置质量：在可承受风险与个人约束下，持续提升商业判断、估值纪律、行为纪律和组合管理能力。**

第一阶段不以短期收益率作为唯一成功标准，而优先观察：

```text
Thesis Quality
Decision Quality
Behavior Discipline
Risk Discipline
Calibration
Review Quality
```

## 2. System Boundary

`invest` 负责：

```text
Investor Behavior Projection
Business / Industry Analysis
Investment Thesis
Valuation / Expected Return
Portfolio / Risk
Company Research
Investment Decision
Investment Review / Feedback
```

`invest` 不负责：

```text
通用 Human Mechanism 定义       → tx / Personal
通用 Framework / Decision Method → meta
职业能力与职业项目               → dw
Personal Objective / Value       → tx
```

## 3. Semantic Object Plane

| Object | Responsibility | Definition Authority |
|---|---|---:|
| **Investment Evidence** | 公司、行业、财务、价格、市场事实、研究资料 | 否 |
| **Investment Source** | 稳定的投资分析方法、投资领域判断规则与本地纪律 | 是 |
| **Company / Thesis** | 对具体标的的研究结论、假设、关键变量、反证条件 | 局部 |
| **Decision Trace** | 买 / 卖 / 持有 / 不行动时的已知信息、理由、风险与仓位逻辑 | 决策记录 |
| **Review / Feedback** | 结果、偏差、归因、能力与运气区分 | 否；用于纠偏 |

固定关系：

```text
Evidence
→ Analysis
→ Thesis
→ Valuation / Risk
→ Decision
→ Reality Result
→ Review
→ Source / Personal Correction Candidate
```

## 4. Core Concerns

### Investor Behavior

只负责投资场景中的行为触发与纪律，例如：

```text
FOMO
Loss Aversion
Anchoring
Confirmation Bias
Overconfidence
Sunk Cost
Crowding
```

通用机制定义来自 `tx`；`invest` 只保存投资场景触发、Slow Path、检查项与行动纪律。

### Business / Industry Analysis

回答：

```text
它靠什么赚钱？
客户为什么付钱？
产业链利润落在哪里？
竞争优势是什么？
优势能持续多久？
增长消耗多少资本？
自由现金流质量如何？
资本配置是否合理？
```

### Valuation / Expected Return

严格区分：

```text
Company Quality
!= Investment Attractiveness
```

评价至少考虑：

```text
Future Cash Flow
Price
Scenario / Probability
Margin of Safety
Expected Return
```

### Portfolio / Risk

单标的判断不能直接推出仓位。单独处理：

```text
Position Size
Diversification
Correlation
Liquidity
Drawdown
Risk Budget
Opportunity Cost
```

### Decision Trace / Review

每次真实决策至少记录：

```text
Known Facts
Thesis
Key Variables
Expected Scenario
Failure Conditions
Valuation
Risk
Position Logic
Action / No Action
```

复盘时区分：

```text
Process Correct / Result Good
Process Correct / Result Bad
Process Wrong / Result Good
Process Wrong / Result Bad
```

防止用结果替代决策质量评价。

## 5. Dependency Contract

```text
meta
→ Method Projection
→ Framework / Decision / Validation

tx / Personal
→ Owner Context Projection
→ Objective / Values / Risk / Behavior / Constraints

invest
→ Domain Judgment
→ Investment Decision
```

因此：

```text
Investment Decision
= Investment Domain Judgment × Personal Suitability
```

Personal 不能替代资产判断；Invest 不能反向定义 Personal Truth。

跨项目关系只消费：

```text
vendor/meta/SYSTEM_ECOSYSTEM.md
```

其 Canonical Source 在 `meta/ecosystem/SYSTEM_ECOSYSTEM.md`。

## 6. SSOT Rules

```text
通用认知方法          → meta
通用人性 / 行为机制   → tx
投资领域规则           → invest Source
具体公司事实           → company / evidence
具体买卖理由           → decision trace
结果                   → review / feedback
```

同一稳定规则只保留一个本地 Source；Company / Decision / Review 只能应用、验证或纠偏。

## 7. Evolution Gate

新增一级 Concern 前必须同时满足：

```text
真实投资过程中重复出现
+ 现有 Concern 无法自然承载
+ 有独立输入 / 输出 / Boundary
+ 会改变真实投资判断或风险控制
+ 增加后总复杂度下降
```

否则降级为：

```text
Rule / Pattern / Checklist / Case / Template / Evidence
```

## 8. Reality Gate

投资系统不能只靠文档成熟度宣布有效。

稳定规则至少经历：

```text
历史案例回测 / 反例检查（按需）
+ 真实 Decision Trace
+ 后续 Reality Review
```

没有现实证据时标记 Candidate / Hypothesis。

## 9. 一句话

> **`invest` 不是预测市场的知识库，而是把 Personal Constraint、投资 Domain Judgment、资本配置决策和 Reality Review 编译成长期可校准能力的系统。**
