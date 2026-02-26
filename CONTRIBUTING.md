# 贡献指南

感谢你考虑为 e-dialect 社区做出贡献！

e-dialect 是一个面向方言保护与学习的开源社区项目群，欢迎来自世界各地的开发者、语言学家、教育者和爱好者参与其中。

本文件是 **e-dialect 组织级贡献指南**，适用于组织下的所有仓库。  

每个仓库可以在自己的 README 中补充仓库特有的说明，但贡献流程与规范以本文件为准。

---

## 0. 许可证与贡献者协议

### 0.1 许可证

e-dialect 组织下的主要代码仓库采用 **GNU Affero General Public License v3.0 (AGPL-3.0)** 或其他 OSI 认证的开源协议。

具体许可证以各仓库根目录的 `LICENSE` 文件为准。

### 0.2 贡献者许可协议（CLA）

为了保障项目的可持续发展，并确保项目管理方拥有合法权利进行商业授权，我们需要贡献者签署贡献者许可协议（CLA）。

#### 个人贡献者（ICLA）

如果你以个人身份贡献代码，且你的贡献不涉及雇主的知识产权，请在提交 Pull Request 前阅读并同意：

- [个人贡献者许可协议 (ICLA)](./ICLA.md)

当你向任意 e-dialect 仓库提交 Pull Request 时，即视为你已阅读、理解并同意 ICLA 条款。

#### 企业贡献者（CCLA）

如果你受雇于某公司，且你的贡献属于职务作品或需代表公司进行，你需要：

1. 让贵公司法务或授权代表阅读并签署：
   - [企业贡献者许可协议 (CCLA)](./CCLA.md)
2. 由项目管理方确认签署后，贵公司员工方可进行贡献。

企业贡献者请在 Pull Request 描述中注明：

- `Contributed on behalf of <Company Name>`

#### 商业授权

e-dialect 项目采用 AGPL-3.0 协议。  

如果你希望在闭源商业产品中使用本项目代码，或需要商业许可（例如私有化部署、SaaS 场景等），请联系项目管理方获取商业授权。

---

## 1. 贡献流程

### 1.1 认领 Issue

1. 在你感兴趣的仓库中，进入 `Issues` 页面。

2. 留意带有 `good first issue` 或 `help wanted` 标签的 Issue，这些通常更适合新贡献者，并附有相关指南。

3. 找到你想解决的 Issue 后，在右侧 Assignees 处点击 `assign yourself`，将该 Issue 分配给自己。这表示你正在尝试解决该问题，避免重复工作。

> 建议：如果你是第一次贡献，先从 `good first issue` 开始，并在评论中简单说明你的计划，便于维护者给予指导。

### 1.2 Fork 与 Clone

1. 点击仓库右上角的 `Fork`，在你的账号下创建该仓库的副本。

2. 将你 Fork 的仓库克隆到本地：

```bash
git clone https://github.com/<你的用户名>/<仓库名>.git
cd <仓库名>
```

如果你不熟悉 Git 命令，可以尝试使用 [GitHub Desktop](https://desktop.github.com/)，它能减少大量命令行操作，但仍建议你逐步学习 Git 基本概念。

### 1.3 创建分支

为了保持提交历史清晰，请为每个独立的改动创建一个新分支：

```bash
git checkout -b <type>-<short-summary>
```

分支命名示例：

- `feat-add-login-page`

- `fix-null-pointer-exception`

- `docs-update-install-guide`

### 1.4 编码与提交

- 按照项目规范进行开发，注意：

  - 遵循各仓库的代码风格与目录结构；

  - 为新功能添加必要的测试；

  - 更新相关文档（README、API 文档等）。

- 提交时请遵循项目的 Commit 规范（见下文）。

### 1.5 推送与创建 Pull Request

1. 将你的分支推送到你 Fork 的仓库：

```bash
git push origin <your-branch-name>
```

2. 在 GitHub 上打开你 Fork 的仓库，页面通常会提示你创建 Pull Request。你也可以手动进入 `Pull requests` 标签页，点击 `New pull request`。

3. 确保：

   - 目标仓库为：`e-dialect/<仓库名>`

   - 目标分支为：`main` 或 `develop`（以该仓库分支策略为准）

   - 源仓库为：`<你的用户名>/<仓库名>`

   - 源分支为：你刚才推送的分支

4. 填写 PR 描述：

   - 清晰描述本次改动的目的与内容；

   - 关联相关 Issue（例如：`Fixes #123` 或 `Closes #456`）；

   - 说明测试方法与结果。

### 1.6 通过 Checks 与 Code Review

- PR 创建后，自动检查（CI/测试）会运行。请留意 Checks 结果，若有失败，根据日志修复问题。

- 维护者会进行 Code Review，并在 PR 中留言：

  - 提出改进建议；

  - 指出潜在问题；

  - 或确认可以合并。

- 请根据 Review 意见更新你的分支。新的提交会自动出现在该 PR 中。

---

## 2. Git 使用规范

### 2.1 Commit 规范

每个 Git 提交信息由 **header** 和可选的 **body** 组成：

```
<header>
<BLANK LINE>
<body>
```

#### Header 格式

Header 是必须的，格式如下：

```
<type>(<scope>): <short summary>
  │       │     │     │
  │       │     │     └─⫸ 简短摘要（原则上使用英文）
  │       │     │       动词原形开头，首字母不大写，结尾无句号
  │       │     │
  │       │     └─⫸ 冒号后必须有一个半角空格
  │       │
  │       └─⫸ 影响范围（scope）：backend、frontend-admin、frontend-user 等
  │
  └─⫸ 类型（type）：build|ci|docs|feat|fix|perf|refactor|test|style|chore|revert

```

#### Type 说明

- `feat`：新功能

- `fix`：Bug 修复

- `docs`：仅文档更新

- `style`：不影响代码含义的格式调整（缩进、空格等）

- `refactor`：既不修复 Bug 也不添加功能的代码重构

- `perf`：性能优化

- `test`：增加或修改测试

- `build`：影响构建系统或外部依赖（如 Dockerfile、docker-compose.yml、Maven/Gradle 配置等）

- `ci`：CI 配置与脚本修改（如 GitHub Actions、GitLab CI 等）

- `chore`：其他不改变 src 或测试代码的修改（如构建脚本、工具配置等）

- `revert`：回退之前的提交

#### Scope 示例

- `backend`：后端服务

- `frontend-admin`：管理后台前端

- `frontend-user`：用户前端

- `h5`：H5 页面

- `ios`：iOS 应用

- `android`：Android 应用

- `mp-weixin`：微信小程序

- `mp-xx`：其他特定小程序（替换掉`xx`）

如果某个改动难以归入以上范围，可以省略 scope。

#### Body 示例

Body 是可选的，用于补充说明：

- 为什么做这个改动；

- 与之前行为的区别；

- 实现细节或注意事项。

示例：

```
fix: address an issue where return value can be null

If an incorrect request body is sent to the server, method xxx may respond
with an empty body due to missing null check in the request parser.
This issue is fixed by adding proper validation and early return.
```

---

## 3. 分支与发布规范

### 3.1 主要分支类型

- `main` / `master`：主分支，保存稳定发布版本。

- `develop`：开发分支，保存最新开发版本，新功能首先合并到此分支。

- `release-YYYYMMDD-<version>`：预发布分支，用于发布前测试与 Bug 修复。

- `feature-<功能编号>`：功能分支，用于开发新功能。

- `hotfix-YYYYMMDD-<关键字>`：热修复分支，用于修复已发布版本的严重 Bug。

> 带星号的分支为临时分支，合并完成后应删除。

### 3.2 功能开发流程

1. 从 `develop` 创建功能分支，如 `feature-GN0101`。

2. 在该分支上进行开发、测试。

3. 开发完成后，创建 PR 合并回 `develop`。

4. 通过 Code Review 与 CI 后，删除该功能分支。

若对同一功能多次迭代开发，可在分支名后加序号，例如：

- `feature-GN0101`

- `feature-GN0101-02`

- `feature-GN0101-03`

### 3.3 预发布与发布

1. 从 `develop` 创建 `release-YYYYMMDD-<version>` 分支。

2. 在该分支上仅允许：

   - Bug 修复；

   - 文档更新；

   - 与发布相关的配置调整。

3. 测试通过后：

   - PR 合并回 `develop`（保存修复）；

   - PR 合并到 `main`（正式发布）。

4. 为 `main` 上的对应提交打 Git 标签，如 `v1.0.0`。

### 3.4 线上热修复

1. 从 `main` 创建 `hotfix-YYYYMMDD-<关键字>` 分支。

2. 在该分支上修复 Bug，并提交 `fix` 类型的 commit。

3. PR 合并到 `main`（修复线上环境）。

4. PR 合并到 `develop`（将修复同步到开发分支）。

5. 删除热修复分支。

---

## 4. Pull Request 规范

- 所有代码变更必须通过 Pull Request 合并，禁止直接向 `main`/`develop` 提交。

- PR 应满足：

  - 有清晰的标题和描述；

  - 关联相关 Issue（使用 `Fixes #xxx` / `Closes #xxx`）；

  - 包含必要的测试用例；

  - 通过所有自动检查（CI/测试）。

- 冲突解决：

  - 必须人工解决冲突，严禁直接使用 “ours” 或 “theirs” 策略；

  - 禁止使用 `git push -f` 或在不理解冲突内容的情况下盲目覆盖他人提交。

---

## 5. 行为准则与社区氛围

我们希望 e-dialect 社区是一个开放、包容、友好的环境。请：

- 尊重不同背景与观点；

- 对事不对人，避免人身攻击或歧视性言论；

- 多一些鼓励与帮助，尤其是对新贡献者。

如需投诉或反馈，请通过以下方式联系项目管理方：

- 在相关仓库创建 Issue，并使用 `meta` 或 `community` 标签；

- 或按照各仓库 README 中提供的联系方式邮件联系。

---

## 6. 其他资源

- [GitHub 官方文档：Fork a repo](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

- [GitHub 官方文档：Creating a pull request from a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)

- [GitHub Community Health Files 文档](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)

再次感谢你的贡献！