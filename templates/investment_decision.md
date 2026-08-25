# Investment Decision Trace

> 用于真实 Buy / Sell / Add / Reduce / Hold / No Action 决策。  
> 执行顺序对齐 [`0_investor/resource_allocation_decision.md`](../0_investor/resource_allocation_decision.md)：先比较坐标，再价值判断，再价格 / 回报，再风险 / 可逆性，最后才到仓位与动作。

## Runtime Index

```text
A. Frame
   A0 Objective / Constraints
   A1 Opportunity Set / Baseline

B. Understand
   B0 Industry / Structure
   B1 Company / Asset Quality
   B2 Shareholder Value Capture

C. Price
   C0 Price / Cost
   C1 Implied Expectations
   C2 Expected Return

D. Protect
   D0 Downside / Permanent Loss
   D1 Margin of Safety
   D2 Optionality / Reversibility

E. Allocate
   E0 Position / Action
   E1 Failure Conditions / Review
```

---

## A0｜Objective / Constraints

```yaml
date:
asset:
capital_objective:
time_horizon:
liquidity_need:
risk_budget:
other_personal_constraints:
```

本次资本配置要解决什么问题：

- 

## A1｜Opportunity Set / Baseline

不做本次动作时，最好的替代项是什么：

```text
Cash:
Index / Benchmark:
Other Asset:
Current Position / No Action:
```

为什么本次候选机会优于最佳替代项：

- 

## B0｜Industry / Structure

只记录与长期价值相关的结构变量：

```text
Demand:
Supply:
Profit Pool:
Competition:
Cycle:
Technology / Regulation:
```

## B1｜Company / Asset Quality

### Known Facts

只记录当时可验证事实：

- 

### Thesis

一句话：

> 

关键变量：

```text
1.
2.
3.
```

### Mechanism

为什么这些变量会影响长期 Earning Power / Free Cash Flow：

- 

## B2｜Shareholder Value Capture

业务创造的价值为什么最终能进入股东回报：

```text
Free Cash Flow Conversion:
Capital Allocation:
Dilution:
Governance:
Debt / Claims Senior to Equity:
```

Value Capture 最大断点：

- 

## C0｜Price / Cost

```text
current_price_or_valuation_reference:
tax_or_transaction_cost:
capital_tied_up:
opportunity_cost:
```

## C1｜Implied Expectations

当前价格已经要求哪些未来事实成立：

```text
Growth:
Margin:
Duration:
ROIC / Capital Efficiency:
Competitive Advantage Duration:
Other Key Expectation:
```

我与市场真正的主要分歧：

- 

## C2｜Expected Return

### Scenarios

```text
Bear:
Base:
Bull:
```

每个情景明确关键变量与概率 / 不确定性。

### Return Sources

```text
Earnings / FCF Growth:
Dividend / Buyback:
Valuation Change:
Other:
```

### Expected Return Judgment

```text
核心假设：
估值区间：
风险调整后的回报吸引力：low | medium | high | unknown
相对最佳替代项：worse | similar | better | unknown
```

## D0｜Downside / Permanent Loss

```text
Permanent Capital Loss:
Balance Sheet / Liquidity Risk:
Business Model Risk:
Valuation Risk:
Governance / Dilution Risk:
Behavior Risk:
```

最坏情况下我可能错在哪里：

- 

## D1｜Margin of Safety

安全边际来自什么，而不是只写一个折价百分比：

```text
Valuation Buffer:
Balance Sheet Resilience:
Business Resilience:
Assumption Conservatism:
Other Error Buffer:
```

最大的估值 / 认知敏感项：

- 

## D2｜Optionality / Reversibility

```text
Liquidity:
Exit Cost:
Cash Reserve / Ability to Add:
Portfolio Correlation:
Ability to Wait:
```

如果判断错了，能否低成本调整：

- 

## E0｜Position / Action

完成 A–D 后才填写：

```yaml
action: buy | sell | add | reduce | hold | no_action
position_before:
position_after:
```

为什么是这个仓位，而不是更大 / 更小：

- 

注意：

```text
Thesis Confidence
!= Position Size
```

仓位必须额外考虑 Risk Budget、Correlation、Liquidity、Personal Constraint、Opportunity Cost 与 Optionality。

## E1｜Failure Conditions / Review

出现以下事实时必须重跑 Thesis / Valuation / Position：

```text
1.
2.
3.
```

What Would Change My Mind：

- 

Review Trigger / Date：

- 

## Decision Quality Check

```text
[ ] 已明确 Objective / Constraints
[ ] 已与最佳替代项比较，而不是孤立评价
[ ] 事实与观点已分开
[ ] Industry / Company Quality / Shareholder Value Capture 已分开
[ ] Thesis 可反证，关键变量明确
[ ] 当前价格隐含预期已写清
[ ] Expected Return 已与上涨故事分开
[ ] Company Quality 与 Investment Attractiveness 已分开
[ ] Permanent Loss / Margin of Safety / Optionality 已分开
[ ] 仓位不是由“看好程度”直接推出
[ ] 已写 Failure Conditions
[ ] 已检查 Personal Constraint
[ ] 没有因为 FOMO / 回本 / 沉没成本推动行动
```

关键项为 `unknown` 时，`no_action` 是正式结果，不为完成模板补故事。

## Future Review

未来只根据当时 Trace 与后续 Reality 复盘：

```text
Result:
Process Correct?:
What Was Luck?:
What Was Skill?:
Which Assumption Failed?:
Which Gate Failed?: A | B | C | D | E | none
Source Correction Candidate?:
Personal Correction Candidate?:
```

复盘必须区分：

```text
Process Correct / Result Good
Process Correct / Result Bad
Process Wrong / Result Good
Process Wrong / Result Bad
```
