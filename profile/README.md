<div align="center">

# E-Dialect

### 地方语言数字化基础设施

*Open, reusable infrastructure for local languages*

**一乡一声，万乡万语。让下一种地方语言，不必再从零开始。**

[官网](https://edialect.top/) ·
[当前计划](https://github.com/orgs/e-dialect/projects/7) ·
[参与贡献](../CONTRIBUTING.md) ·
[社区治理](../GOVERNANCE.md) ·
[全部仓库](https://github.com/orgs/e-dialect/repositories)

</div>

---

## 让地方语言数字化不再是一次性工程

一种地方语言、一批资料、一支团队，再重新搭建一遍采集、整理、校勘、发布和协作
系统——许多地方语言项目仍在重复解决相似的工程问题。懂语言的本地社区往往缺少完整
工具链，通用技术平台又难以替每一种语言维护具体知识。

**E-Dialect 是一个开放工程社区。** 我们把地方语言数字化中反复出现的资料处理、协同
校勘、公众共建、智能辅助和可追溯治理，沉淀为可以复用、部署和继续演进的软件与规范。
这里可以承载不同语言、产品和研究方向的多个 initiative；**乡声万语是当前重点计划，
但不等同于整个 E-Dialect。**

> **平台提供可复用的方法、工具与证据链；真正懂这门语言的本地社区负责知识与判断。**

## 当前重点计划：乡声万语

[乡声万语](https://github.com/orgs/e-dialect/projects/7) 正在以莆仙方言为当前锚点，把真实
资料、真实用户旅程和真实协作压力带入通用工具建设。目标不是把一个地方产品复制成多个
皮肤，而是验证一条能够适应不同文字、音系、资料条件和社区结构的数字化路径。

### 从原始资料到持续共建

`原始资料 → 协同校勘 → 可信结构化数据 → 公众使用与补证 → 新一轮整理`

| 环节 | 项目 | 作用 |
|---|---|---|
| 专业资料整理 | [万语校坊](https://github.com/e-dialect/wanyu-proofreader) | 面向地方志团队、研究者和整理团队的协同校勘平台，支持 PDF/CSV 导入、多人独立校对、差异发现、仲裁与导出。 |
| 公众使用与可信共建 | [乡声集盒](https://github.com/e-dialect/xiangsheng-box) | 面向普通用户的地方语言工具与共建平台，通过“听、查、录”等真实使用过程沉淀带来源、地域背景和证据的资料。 |
| 地方应用验证 | [兴化语记](https://github.com/e-dialect/xiangsheng-box/blob/main/docs/HINGHWA.md) | 面向莆仙方言的旗舰地方入口；持续把具体语言场景的需求反馈给通用产品、数据模型与协作流程。 |

万语校坊不是乡声集盒的管理后台，兴化语记也不是一次性演示。它们分别承担专业整理、
通用共建和地方应用验证的职责，并通过明确的数据与产品边界协作。

## 实验中的智能能力

我们也在探索低资源条件下的语义检索、语音识别与合成，以及知识辅助校验：

- [hinghwa_semantic_retrieval](https://github.com/e-dialect/hinghwa_semantic_retrieval)：莆仙方言语义检索实验；
- [ipa_tts_minimal](https://github.com/e-dialect/ipa_tts_minimal)：轻量 IPA-to-TTS 推理与部署验证；
- [Voice_Whisper](https://github.com/e-dialect/Voice_Whisper)：多来源语音处理能力的集成实验。

这些仓库是仍在研究和工程验证中的能力模块，不包装成一个已经成熟的“通用智能引擎”。
模型、数据、第三方代码和生成物也不因仓库公开而自动适用同一种许可证。

## 我们如何做工程

- **共性技术与具体语言知识解耦**：核心模型和组件面向多语言复用，正字、读音、释义和
  文化语境由相应社区维护。
- **来源先于结论**：原始材料、用户提交、整理判断和自动推断保留各自身份，不用投票或
  模型分数自动裁定唯一答案。
- **AI 辅助而不冒充证据**：AI 可以发现问题、生成候选和减少重复劳动；高风险结论仍需
  可追溯材料与人工审核。
- **把部署和协作也当作产品**：不仅发布代码，也建设权限、审计、贡献流程、测试与回滚
  能力，让地方团队能够真正接手。

## 参与共建

无论你熟悉代码、语言，还是自己的家乡，都可以找到具体入口：

- **开发者**：参与前后端、基础设施、数据工具、RAG 与语音工程。先阅读
  [贡献指南](../CONTRIBUTING.md)，再到[乡声万语项目板](https://github.com/orgs/e-dialect/projects/7)
  或对应仓库认领 Issue。
- **语言学研究者与资料整理者**：帮助定义音系、正字、来源、数据质量与审校规则；可从
  [方言数字基建贡献路线](https://github.com/e-dialect/xiangsheng-box/blob/main/docs/CONTRIBUTOR_TRACK_COMMONS.md)
  和[万语校坊](https://github.com/e-dialect/wanyu-proofreader)开始。
- **地方社区与方言使用者**：提出真实使用场景，查、听、录下家乡表达，并补充地域背景
  和来源证据；参见[乡声共创路线](https://github.com/e-dialect/xiangsheng-box/blob/main/docs/CONTRIBUTOR_TRACK_EXPERIENCE.md)。

第一次参与 Git/GitHub 协作，可以先进入
[Git / GitHub 协作练习](https://github.com/e-dialect/code-contributing-practice)。

## 社区、治理与权利边界

- **E-Dialect** 是开放 GitHub 工程社区，不等同于任何公司，也不等同于某一个 initiative。
- **乡声万语** 是当前重点计划；未来可以并行发起其他语言、工具或研究 initiative。
- 目前乡声万语相关商业合作、签约与交付由**北京塔聚科技有限责任公司**作为商业/法律
  承载主体；具体权利义务以实际合同、许可证、CLA 和知识产权文件为准。

各仓库分别依其 `LICENSE`、`LICENSING.md` 和路径级声明授权。由项目有权授权的原创应用
与网络服务代码通常采用 `AGPL-3.0-only`；第三方代码继续适用上游条款。软件许可证和
代码 CLA **不自动覆盖**数据、语料、词典内容、录音、个人信息、模型权重、商标或 Logo。
详见[许可证政策](../LICENSING.md)、[资产与数据政策](../ASSET_AND_DATA_POLICY.md)和
[开源承诺](../OPEN_SOURCE_COMMITMENT.md)。

## 联系

- 在相关仓库创建 Issue；
- 邮件：[edialect@edialect.top](mailto:edialect@edialect.top)。

<div align="center">

**第一种地方语言走过的长路，应当成为下一种地方语言可以复用的基础设施。**

</div>
