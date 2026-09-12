# E-Dialect 治理与交付机制

本文是 E-Dialect 的组织级治理基线，并记录当前 initiatives 的责任映射。它用于明确 ownership、决策、升级和验收责任，不替代各仓库的技术规范、许可证、CLA、合同或 initiative charter。

## 1. Organization-wide baseline

### 1.1 角色

- **Repository Maintainer**：维护仓库边界、质量与发布规则。
- **Project / Initiative Owner**：维护跨 Issue 或跨仓库目标、优先级与协作关系。
- **Accountable Owner**：对一个 Tracking、Epic 或 Work Package 的范围、拆分、风险、证据和 Gate 负责。
- **Steering**：仅当 initiative 明确定义时存在，负责重大方向、升级事项与最终 Acceptance。

这些角色可以由同一人兼任，也可以按仓库或 initiative 分开；具体账号由对应仓库或 initiative 声明，不在组织基线中永久写死。

### 1.2 Ownership

GitHub 原生 Assignee 是正式 ownership 信号：

- **Tracking / Epic Assignee** 可以表示 accountable ownership，负责 scope、拆分、节奏、风险、证据与 Gate，不表示该人亲自实现所有子任务。
- **Leaf Assignee** 表示当前实际推进实现、调研、QA 或数据工作的负责人。
- 没有 Assignee 的 Leaf 不视为已被正式认领；不要仅为填满字段而猜测负责人。

正文可以解释责任语义，但不能成为唯一 ownership source。

## 2. Observation、Decision 与 Directive

Repository Maintainer、Project Owner 或 Steering 的一般意见默认是 **Observation**，由对应 Accountable Owner 结合目标、证据与当前节奏判断，不自动改变正在执行的工作。

- **Observation**：建议、风险提示或待观察信号。
- **Decision**：对已升级选项作出的选择。
- **Directive**：需要立即改变当前范围、顺序或停止条件的明确指令。

只有明确标记为 Directive 的输入才自动改变当前计划。观察意见不能被执行者自行放大为隐含命令。

## 3. 可逆决策模板

需要 Repository Maintainer、Project Owner 或 Steering 判断时使用以下结构：

```markdown
## Context
当前事实、证据与需要决定的问题。

## Options
可行选项及各自代价。

## 负责人建议
Accountable Owner 的推荐项与理由。

## Reversibility
是否可逆；回退成本与最后安全回退点。

## Deadline
YYYY-MM-DD HH:mm TZ

## Default action if no response
截止时间未收到回复时将执行的动作。
```

对可逆、未触发升级条件的事项，Accountable Owner 可在期限后按推荐方案继续推进并留下记录。普通执行事项不应因等待无关角色无限停摆。

## 4. 必须升级的事项

下列事项必须升级到当前仓库或 initiative 已定义的 Repository Maintainer、Accountable Owner 或 Steering，不适用默认推进：

- 品牌、公关表述或对外承诺；
- 隐私、知情同意、未成年人、录音与历史媒体授权；
- `LICENSE`、ICLA、CCLA、知识产权或商业授权条款；
- 商业合同、采购、付款或其他资金事项；
- 不可逆架构决定或破坏性数据迁移；
- 跨仓库 public contract 的重大变更；
- P0 目标或范围的重大变化；
- 同一目标连续两次 Gate 失败；
- 只有上级责任角色能取得的外部资源；
- 重大数据丢失、法律/隐私风险、公开事件或是否停止服务。

## 5. 风险与人工审查

- **R0**：低风险文档、样式或局部配置。Agent review + CI + 实际运行或视觉检查。
- **R1**：常规逻辑。独立 agent review + tests + 作者走完目标行为或关键用户旅程；不强制第二名人类逐行 review。
- **R2**：迁移、认证、权限、访客合并、同意/来源、删除、生产发布、破坏性导入等高风险变更。除 agent review 与测试外，必须有人类针对关键路径审查，并提供 staging、backup、rollback 等适用证据。

R2 必须由对应 Repository Maintainer / Accountable Owner 验收；若 initiative 定义了 Steering escalation，再按其治理规则升级。

任何风险等级都必须如实填写 `Not manually verified`，不得用“AI 已检查”代替实际证据。Human review 应按风险与关键路径定向，不按 diff 行数机械执行。

## 6. Current initiative mapping: 乡声万语

### Scope

- `e-dialect/xiangsheng-box`
- `e-dialect/wanyu-proofreader`
- [Project #7 · 乡声万语 · 2027 春节冲刺](https://github.com/orgs/e-dialect/projects/7)

### Current responsibility mapping

- Steering：[@lin594](https://github.com/lin594)
- 乡声集盒 accountable owner：[@aB0T-bupt](https://github.com/aB0T-bupt)
- 万语校坊 accountable owner：[@L8848-Li](https://github.com/L8848-Li)

默认升级路径：

```text
Member
→ corresponding accountable owner
→ @lin594
```

Shared 是 Project 中的跨产品 workstream，不是第三个直属团队。上述账号是当前乡声万语 initiative 的责任映射，不是 E-Dialect 所有未来仓库的永久治理结构；其它仓库或 initiative 应自行声明 maintainer、owner 与 escalation path。

### Operating cadence

乡声万语当前每周由两个 accountable owner 分别异步更新：

```text
Done / Demo / Blocked / Next / Need Steering Decision
```

约每两周进行一次 Demo Gate。Gate 必须展示可复核的真实证据，例如实际页面、真机路径、数据样本、模型输出或可复现实验；PPT 和口头进度不能单独通过 Gate。

乡声万语的 Epic / Work Package 应定义 **Demo Moment**。成员支持采用 L0–L3 分级；能力不足时缩小 Leaf 粒度，不降低 Acceptance Gate。其它 initiative 可按自身规模和风险定义 cadence 与支持方式。
