# Investment Cognitive & Decision System

> 角色：Owner 的 **Investment Cognitive & Decision System｜投资认知与决策系统**。
>
> 当前阶段不是“炒股训练”，而是 **Investor Formation｜投资者形成期**：先训练心性、商业/行业分析、估值判断与判断校准；真实资本配置与交易执行暂不作为主线。

## 1. 当前目标

```text
Temperament
× Business Judgment
× Valuation Judgment
× Capital Allocation
→ Investment Capability
```

当前训练权重：

```text
Investor Behavior / Temperament      30%
Business / Industry Analysis         45%
Valuation / Expected Return          15%
Decision Trace / Review              10%
Portfolio / Trading                  暂缓
```

核心原则：

> **先成为能理解商业、承受不确定性、形成可证伪判断的人，再讨论真实交易。**

## 2. 系统闭环

```text
Company / Industry Reality
→ Business / Industry Analysis
→ Thesis
→ Valuation / Expected Return
→ Simulated Decision / No Action
→ Later Reality
→ Review
→ Source Correction
```

行为侧：

```text
Human Mechanism（tx）
→ Investor Temperament Projection
→ Trigger / Slow Path / Judgment Discipline
→ Review
→ Reality Feedback
```

## 3. 当前核心入口

| 当前问题 | 入口 |
|---|---|
| 系统对象、定义权、边界 | [`SYSTEM_ARCHITECTURE.md`](SYSTEM_ARCHITECTURE.md) |
| AI 权限、Owner Gate | [`AGENTS.md`](AGENTS.md) |
| 投资教练 / 每周文章训练 | [`0_investor/investment_coach.md`](0_investor/investment_coach.md) |
| **从机会比较到仓位的统一执行顺序** | [`0_investor/resource_allocation_decision.md`](0_investor/resource_allocation_decision.md) |
| 心性 / 投资判断纪律 | [`0_investor/temperament.md`](0_investor/temperament.md) |
| 商业模式分析 | [`1_business/business_analysis.md`](1_business/business_analysis.md) |
| 行业结构分析 | [`1_business/industry_analysis.md`](1_business/industry_analysis.md) |
| 估值判断 | [`2_valuation/valuation_judgment.md`](2_valuation/valuation_judgment.md) |
| 无需实盘的研究 Thesis | [`templates/research_thesis.md`](templates/research_thesis.md) |
| 真实资本配置 Decision Trace | [`templates/investment_decision.md`](templates/investment_decision.md) |
| 训练复盘 | [`reviews/training_review.md`](reviews/training_review.md) |

## 4. 当前四条训练主线

### A. Temperament｜心性

训练目标不是“没有情绪”，而是：

> **在不确定、高波动、延迟反馈和观点冲突中，判断质量不被自证、FOMO、损失厌恶、从众和结果反馈接管。**

### B. Business Judgment｜商业判断

固定追问：

```text
谁付钱？
为什么付钱？
公司靠什么赚钱？
成本与瓶颈是什么？
利润为什么留在这里？
竞争者为什么抢不走？
增长需要多少资本？
规模扩大后经济性变好还是变差？
```

### C. Industry Judgment｜行业判断

固定沿：

```text
需求 → 供给 → 产业链 → 利润池 → 竞争格局 → 壁垒 → 技术 / 监管 / 周期
```

目的不是预测板块涨跌，而是判断利润如何形成、迁移和消失。

### D. Valuation｜估值判断

始终区分：

```text
Good Company != Good Investment
```

估值的第一任务不是算出“精确价格”，而是识别：

```text
当前价格隐含什么预期？
我必须相信哪些关键假设，价格才成立？
如果核心变量低于预期，结果会怎样？
```

### Cross-concern Runtime｜统一资本配置顺序

局部 Source 不改定义权，运行时统一按：

```text
A. Frame      → Objective / Constraints / Alternatives
B. Understand → Industry / Company / Shareholder Value Capture
C. Price      → Price / Implied Expectations / Expected Return
D. Protect    → Permanent Loss / Margin of Safety / Optionality
E. Allocate   → Position / Failure Conditions / Review
```

因此：

```text
Good Company
!= Good Investment
!= Right Position Size
```

## 5. 当前训练循环

```text
每周 2 篇 Investment Coach 高质量文章 → Evidence / Candidate + 训练题
→ 每周 1 个投资心性机制
→ 每周 1 家公司商业模式
→ 每 2 周 1 个行业结构
→ 每月 1 份完整 Research Thesis
→ 3~6 个月后 Reality Review
```

评价重点：

```text
关键变量有没有找对？
机制有没有讲通？
反证条件是否清楚？
概率与不确定性是否被诚实表达？
后续 Reality 为什么与当时判断不同？
```

短期股价涨跌不作为训练是否成功的主指标。

## 6. 当前不做什么

```text
不以选股 / 短线收益为训练中心
不提前硬编码仓位百分比、止损点和交易频率
不把历史人格评估写成永久 Investor Identity
不因为目录完整提前创建空 companies / portfolio / decisions
不把宏观变量直接映射成买卖动作
```

当真实投资资产与持续 Decision Trace 出现后，再自然生长：

```text
3_portfolio/
companies/
decisions/
```

## 7. Dependency

```text
meta → 通用建模 / 决策 / 验证方法
tx   → Objective / Human Mechanism / Personal Constraint
invest → Investment Domain Judgment + Training + Decision + Review
```

其中资源配置运行顺序消费：

```text
meta@dev/methods/resource-allocation-decision.md
→ invest@dev/0_investor/resource_allocation_decision.md
→ templates/investment_decision.md
```

通用人性定义归 `tx`；`invest` 只保存投资场景 Projection。

## 8. 一句话

> **当前先训练“心性—商业—行业—估值—校准”的认知链，并用统一资源配置顺序把它们编排成可执行决策；不把投资系统做成交易系统或股票收藏夹。**