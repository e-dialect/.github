# E-Dialect 治理与交付机制

本文定义 E-Dialect 组织与“乡声万语”计划的轻量治理基线。它用于明确决策、升级和验收责任，不替代各仓库的技术规范、许可证、CLA 或合同。

## 1. 角色与责任

### Steering / Acceptance / Gatekeeper

当前 Steering：[@lin594](https://github.com/lin594)。

Steering 负责：

- 确认 Objective、Scope、Gate 与重大方向；
- 对需要升级的决策给出 Decision 或 Directive；
- 在 Demo Gate / Release Gate 进行最终 Acceptance；
- 协调只有 Steering 能取得的外部资源。

Steering **不负责**日常项目管理、逐个分配叶子任务、审核每一个 PR，或替代 @aB0T-bupt / @L8848-Li 做可逆的执行判断。

### 产品责任账号

- [@aB0T-bupt](https://github.com/aB0T-bupt)：乡声集盒 Sprint Tracking 与 Epic 拆解
- [@L8848-Li](https://github.com/L8848-Li)：万语校坊 Sprint Tracking 与 Epic 拆解

@aB0T-bupt 与 @L8848-Li 分别对本产品 Sprint Tracking 负责，把 Epic 拆为可认领的 Leaf，维护优先级、风险、证据与 Demo Moment，并组织日常 review。Epic 的 Assignee 表示 accountable owner，不表示由一人实现全部工作。

问题与决策的默认升级路径是：

```text
Member → @aB0T-bupt / @L8848-Li → @lin594
```

Shared 是 Project 中的协作 workstream，不是第三个直接团队，也不另设负责人。@lin594 默认只与 @aB0T-bupt、@L8848-Li 对接。

## 2. Observation、Decision 与 Directive

Steering 的一般意见默认是 **Observation**：@aB0T-bupt / @L8848-Li 记录并结合目标、证据和当前节奏判断，不立即改变 Sprint。

- **Observation**：建议、风险提示或待观察信号。
- **Decision**：对已升级选项作出的选择。
- **Directive**：需要立即改变当前范围、顺序或停止条件的明确指令。

只有明确标记为 Directive 的输入才自动改变正在执行的 Sprint。观察意见不能被执行者自行放大为隐含命令。

## 3. 可逆决策模板

需要 Steering 判断时使用以下结构：

```markdown
## Context
当前事实、证据与需要决定的问题。

## Options
可行选项及各自代价。

## 负责人建议
@aB0T-bupt 或 @L8848-Li 的推荐项与理由。

## Reversibility
是否可逆；回退成本与最后安全回退点。

## Deadline
YYYY-MM-DD HH:mm TZ

## Default action if no Steering response
截止时间未收到回复时将执行的动作。
```

对可逆、未触发升级条件的事项，@aB0T-bupt 或 @L8848-Li 在期限后按推荐方案继续推进并留下记录。不要让普通执行事项因等待 @lin594 无限停摆。

## 4. 必须升级的事项

下列事项必须由 @aB0T-bupt 或 @L8848-Li 升级给 @lin594，不适用默认推进：

- 品牌、公关表述或对外承诺；
- 隐私、知情同意、未成年人、录音与历史媒体授权；
- `LICENSE`、ICLA、CCLA、知识产权或商业授权条款；
- 商业合同、采购、付款或其他资金事项；
- 不可逆架构决定或破坏性数据迁移；
- 共享 X/W Contract 的重大变更；
- P0 目标或范围的重大变化；
- 同一目标连续两次 Gate 失败；
- 只有 Steering 能取得的外部资源；
- 重大数据丢失、法律/隐私风险、公开事件或是否停止服务。

## 5. 节奏与验收

@aB0T-bupt 与 @L8848-Li 每周分别异步更新一次：

```text
Done / Demo / Blocked / Next / Need Steering Decision
```

约每两周进行一次 Demo Gate。Gate 必须展示可复核的真实证据，例如实际页面、真机路径、数据样本、模型输出或可复现实验；PPT 和口头进度不能单独通过 Gate。

所有 Epic / Work Package 应定义 **Demo Moment**：验收者可以在何时、以什么步骤看到什么结果。遇到能力差异时使用 L0–L3 支持分级，并通过缩小 Leaf 粒度帮助成员进入 L1；不降低 Acceptance Gate。

## 6. 风险与人工审查

- **R0**：低风险文档、样式或局部配置。Agent review + CI + 实际运行或视觉检查。
- **R1**：常规逻辑。独立 agent review + tests + 作者走完完整用户旅程或目标行为；不强制第二名人类逐行 review。
- **R2**：迁移、认证、权限、访客合并、同意/来源、删除、生产发布、破坏性导入等高风险变更。除 agent review 与测试外，必须有人类针对关键路径审查、staging/backup/rollback 证据，并由对应的 @aB0T-bupt 或 @L8848-Li 验收。

任何风险等级都必须如实填写 `Not manually verified`，不得用“AI 已检查”代替实际证据。
