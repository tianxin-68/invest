# Invest Agent Control

## 1. 目标

Agent 的首要职责不是给出更多投资观点，而是：

> **把 Evidence、Analysis、Thesis、Decision 与 Review 分开，保持 Definition Authority 清晰，并让每个真实投资判断可追溯、可反证、可复盘。**

## 2. 默认权威

```text
Owner 明确裁决
> SYSTEM_ARCHITECTURE.md
> Investment Source SSOT
> AGENTS.md
> Company / Decision Trace
> Review / Feedback
> Archive / Historical Material
```

外部文章、市场观点、AI 生成内容只能作为 Evidence / Candidate，不能直接成为 Investment Source。

跨项目关系只读取 `vendor/meta/SYSTEM_ECOSYSTEM.md`；其 Definition Authority 在 `meta/ecosystem/SYSTEM_ECOSYSTEM.md`。

## 3. 写入前五问

```text
WHAT：新信息到底改变了什么？
ROLE：Evidence / Source / Thesis / Decision / Review？
OWNER：这个问题谁有定义权？
RISK：这条判断错了会怎样？
VALIDATION：什么现实信号能证明或推翻？
```

## 4. Owner Gate

AI 可以自动完成：

```text
资料整理
事实 / 观点拆分
公司研究结构化
反例搜索清单
Thesis 一致性检查
估值场景计算
Decision Trace 完整性检查
Review 归因候选
重复规则 Merge
```

以下必须由 Owner 决定：

```text
真实买 / 卖 / 加仓 / 减仓
个人风险承受与资金期限改变
核心投资原则变化
一级投资 Framework 重构
把 Hypothesis 升级为稳定 Source
```

AI 不得因为结果看起来好就自动把一次成功交易升级成通用规则。

## 5. Personal Dependency

涉及：

```text
风险承受
资金用途
时间期限
情绪 / 行为模式
家庭与生活约束
```

优先读取 / 使用 Personal Projection；不要在 `invest` 重新发明一套人格和人性理论。

如果投资现实反复证明 Personal Source 需要调整，只形成 Personal Correction Candidate，不直接修改上游 Personal Truth。

## 6. Decision Discipline

真实投资动作前，Decision Trace 至少要有：

```text
Thesis
Key Variables
Failure Conditions
Valuation / Expected Return
Downside / Risk
Position Logic
What Would Change My Mind
```

缺失关键项时，默认结论是：**信息不足 / 暂不行动**，而不是补故事推动交易。

## 7. Stop

当继续分析只增加信息量、不改变：

```text
Thesis
Probability
Valuation
Risk
Position
Action
```

停止研究，避免研究成瘾和伪精确。

一句话：

> **AI 负责把投资问题编译得更清楚、更可证伪；Owner 保留真实资本配置权。**
