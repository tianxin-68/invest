# Resource Allocation Decision｜Investment Domain Framework

> **职责**：组织投资域现有 Industry / Business / Valuation / Risk / Decision Source 的消费顺序，形成低带宽、可执行的资本配置决策链。  
> **Definition Authority**：仅限 Investment Domain；不取得跨域 Meta Definition Authority。

## 1. Objective

投资不是回答“公司好不好”，而是：

```text
在资本 / 风险 / 时间约束下
→ 相比现金、指数与其他机会
→ 这个资产能创造并由股东捕获多少价值
→ 当前价格已经包含什么预期
→ 风险调整后的 Expected Return 是否值得
→ 最坏情况下会失去什么、是否可逆
→ 最后才决定仓位与行动
```

核心约束：

```text
Good Company
!= Good Investment
!= Right Position Size
```

## 2. Two-level Runtime Index｜两层执行索引

| Index | 投资决策对象 | 执行问题 |
|---|---|---|
| **A0** | Objective / Constraints | 资金期限、流动性、风险预算、不可承受损失是什么？ |
| **A1** | Opportunity Set / Baseline | 不买它，现金、指数或其他资产哪个是更好的替代项？ |
| **B0** | Industry / Structure | 需求、供给、利润池、竞争、周期、监管、技术变化如何？ |
| **B1** | Company / Asset Quality | 商业模式、竞争优势、资本效率、管理层与财务质量如何？ |
| **B2** | Shareholder Value Capture | 业务创造的价值最终能否进入股东现金流？稀释、资本配置、治理会不会截断？ |
| **C0** | Price / Cost | 当前价格、税费、资金占用和替代收益成本是什么？ |
| **C1** | Implied Expectations | 当前价格已经要求多高增长、利润率、持续期与竞争优势？ |
| **C2** | Expected Return | 回报来自盈利增长、现金分配、估值变化中的哪几项？风险调整后还剩多少吸引力？ |
| **D0** | Downside / Permanent Loss | 永久资本损失可能通过什么路径发生？ |
| **D1** | Margin of Safety | 对业务、估值和认知不确定性留了多少缓冲？ |
| **D2** | Optionality / Reversibility | 流动性、现金储备、退出成本和未来加减仓自由度如何？ |
| **E0** | Position / Exposure | 即使值得买，为什么是这个仓位而不是更大 / 更小？ |
| **E1** | Failure Conditions / Review | 哪些事实出现后必须重跑 Thesis / Valuation / Position？ |

执行顺序固定：

```text
A Frame
→ B Understand
→ C Price
→ D Protect
→ E Allocate
```

禁止：

```text
看好行业
→ 看好公司
→ 直接买 / 重仓
```

## 3. Five Investment Gates｜五道门

### Gate A｜比较坐标成立吗？

必须先知道：

```text
Objective
Personal Constraint
Best Alternative
```

没有替代项比较时，“便宜 / 优秀 / 值得买”都缺乏决策坐标。

### Gate B｜价值创造与股东捕获成立吗？

```text
Industry Profit Pool
→ Company Competitive Position
→ Earning Power / Free Cash Flow
→ Capital Allocation / Dilution / Governance
→ Shareholder Value Capture
```

AI、能源、消费等大趋势即使完全正确，也不能跳过公司与股东的 Capture Path。

### Gate C｜价格是否透支？

固定拆开：

```text
Facts
!= Market Expectations
!= Price
```

先反推当前价格要求哪些未来事实成立，再判断自己与市场真正的分歧。

### Gate D｜错了能否承受？

分开看：

```text
Permanent Loss Risk
Margin of Safety
Reversibility / Liquidity
```

风险不是“会不会波动”，而是判断错后是否造成不可恢复的资本损失或被迫退出。

### Gate E｜仓位是否与证据匹配？

```text
Thesis Confidence
!= Position Size
```

仓位还必须考虑：

```text
Risk Budget
Correlation
Liquidity
Personal Constraint
Opportunity Cost
Optionality
```

## 4. Runtime Algorithm｜6 问现场算法

每次研究准备进入 Decision 时，只问：

```text
1. 我为什么要配这笔资本？不买的最好替代项是什么？
2. 价值怎么产生，并且怎么进入股东回报？
3. 当前价格已经相信了什么？我和市场真正分歧在哪里？
4. Expected Return 从哪里来？哪几个变量最敏感？
5. 最坏的永久损失路径是什么？我是否有安全边际和退出自由？
6. 如果仍值得做，为什么是这个仓位？什么事实出现后重跑？
```

任何关键项为 `unknown` 时：

```text
unknown
→ no_action / small_exposure / keep_optionality
```

具体动作仍由 Owner Gate 决定。

## 5. Decision Standards｜投资域裁决标准

1. **必须相对比较**：资产吸引力必须相对现金、指数或其他机会判断；
2. **公司质量与投资吸引力分离**：好公司不能替代价格判断；
3. **价值创造与股东价值捕获分离**：业务繁荣不能替代自由现金流、稀释、资本配置与治理判断；
4. **趋势、公司、价格、仓位四层不得跨层跳跃**；
5. **Expected Return 是正式对象**：不能只谈故事、目标价或上涨空间；
6. **Permanent Loss、Margin of Safety、Optionality 分开判断**；
7. **仓位独立于 Thesis**：看好程度不能直接透传为重仓；
8. **`unknown / no_action` 是正式结果**；
9. **结果与过程分离复盘**：一次赚钱不能证明过程正确，一次亏损也不能自动证明过程错误。

## 6. Relationship to Existing Invest Sources

本 Framework 不复制各 Concern 的 Domain Truth，只编排消费顺序：

```text
B0 Industry
→ 1_business/industry_analysis.md

B1 / B2 Business + Value Capture
→ 1_business/business_analysis.md

C1 / C2 Valuation / Expectations
→ 2_valuation/valuation_judgment.md

E Decision Trace
→ templates/investment_decision.md

Behavior / Slow Path
→ 0_investor/temperament.md
→ 0_investor/behavior_discipline.md
```

它的角色是 **Investment Domain Orchestrator / Runtime Decision Framework**，不是第二份 Business、Valuation 或 Risk Source。

## 7. Meta Promotion Boundary

本框架首先在 `invest` 内运行、消费和校准。

```text
Local Invest Reality
→ Local Framework Use
→ Reality / Review Evidence
→ 可迁移 Learning
→ META_CANDIDATE
→ Owner Gate
→ 才可能形成 Meta Source
```

仅因为它可以类比 Career，不足以取得 Meta Definition Authority。

## 8. Boundary

本文件不：

```text
给具体股票评分
设置固定仓位百分比
定义止损价格
自动触发交易
把新闻或名家观点升级为 Source
```

真实资本配置必须满足 `AGENTS.md` Owner Gate。

一句话：

> **先比较替代项，再判断价值创造与股东捕获；把价格、预期、回报、风险、可逆性拆开，最后才决定仓位。**