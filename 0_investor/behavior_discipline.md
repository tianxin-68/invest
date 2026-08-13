# Investor Behavior Discipline｜投资场景行为纪律

> 角色：**Investment Source**。只定义投资场景中的触发、Slow Path 与行动纪律；通用人性机制仍由 `tx` 定义。
> 来源：Notion `40_invest` 历史材料的有效增量 + 当前 `invest` Architecture / Decision Trace 校验。

## 一句话

> **行动冲动不是投资证据；只有 Thesis、Probability、Valuation、Risk、Position 或 Personal Constraint 发生了可说明的变化，才有理由从 `no_action` 切换到交易动作。**

## 1. 高频触发

出现以下任一信号，先进入 Slow Path，不直接交易：

```text
FOMO / 怕错过
想回本 / 不愿承认判断错误
短期涨跌后信心剧烈变化
通过买卖缓解焦虑
研究到想获得 100% 确定性
因为已经投入很多而继续加码
因为别人赚钱 / 市场热闹而改变计划
```

这些是投资场景触发器，不自动推断为 Owner 的稳定人格事实。历史 Notion 中的个人评估只作为 Candidate Evidence，必须由当前 Reality 重新验证。

## 2. Slow Path

```text
1. 先写：为什么是现在？
2. 分开：事实变化 / 价格变化 / 我的情绪变化
3. 问：Thesis / Probability / Valuation / Risk / Position 到底哪一项变了？
4. 没有可说明变化 → no_action
5. 有变化 → 更新 Decision Trace，再决定 buy / sell / add / reduce / hold
```

默认允许：

> **错过机会，不等于发生资本损失。**

所以不能为了消除“以后会不会后悔”的想象而强行建立仓位。

## 3. 规则内亏损 vs 规则外亏损

复盘时先分：

```text
Process Correct + Result Bad
→ 先检查概率、假设和运气，不做人格审判

Process Wrong + Result Good
→ 仍然算流程失败，不能因为赚钱就强化错误行为

Rule Breach
→ 找触发器、闸门和环境变量，修行为接口
```

**结果不能反向替代当时的决策质量。**

## 4. 行为纪律

- `no_action` 是正式动作，不是“什么都没做”。
- 不用交易频率缓解焦虑；固定复审节奏可以作为局部工具，但不是全局硬编码。
- 不把固定“停手 3–7 天”之类惩罚写成稳定规则；真正目标是找到触发器并降低复发概率。
- 不用“学徒 / 高手”身份推动动作；能力只看 Decision Trace、Review 与长期 Reality Evidence。
- 通用情绪调节、损失厌恶、沉没成本等机制引用 `tx`，本文件只保留投资 Projection。

## 5. 反馈信号

```text
Rule Breach Count
Impulse → Decision Trace 的延迟
Price-only Trigger Count
No-action 后是否出现后悔驱动的追单
Process Correct / Wrong 的长期占比
```

反馈只用于校准纪律，不用短期收益率证明“我已经会投资”。

## 6. 边界

以下不是本文件的定义权：

```text
个人风险承受 / 家庭资金期限 → tx / Owner
单标的仓位与风险预算       → 3_portfolio
公司是否值得买             → Business / Thesis / Valuation
通用人性机制               → tx
真实买卖动作               → Owner Gate
```

一句话：

> **先证明“为什么要动”，再决定“怎么动”；如果变化只发生在情绪，不发生在投资变量，默认不动。**