# CLA Personal-Information Protection Impact Assessment Record
# CLA 个人信息保护影响评估记录

**Assessment date / 评估日期：2026-09-14**  
**Scope / 范围：planned e-dialect ICLA workflow; not yet activated / 拟上线的
e-dialect ICLA 流程；尚未启用**

This public record contains no contributor personal data. It is a lightweight
governance assessment, not legal advice or a substitute for advice on a
specific processing activity.

本公开记录不包含任何贡献者个人信息。它是一份轻量治理评估，不构成法律意见，也不
替代针对具体处理活动的专业意见。

## Processing activity and purpose / 处理活动与目的

e-dialect plans to use the SAP-provided CLA Assistant hosted service and
GitHub authentication to record explicit acceptance of ICLA Version 1.0. The
purposes are to verify the contributor's authenticated identity, record the
agreement version and acceptance, establish an auditable code-contribution
rights chain, conduct necessary compliance audits, and handle related disputes
when necessary.

e-dialect 计划使用由 SAP 提供的 CLA Assistant 托管服务和 GitHub 身份验证，记录
ICLA 1.0 版的显式接受。处理目的为验证贡献者经身份验证的账号，记录协议版本与接受，
建立可审计的代码贡献权利链，以及进行必要的合规审计和相关争议处理。

## Data minimization / 数据最小化

The project configuration is limited to legal name; GitHub-authenticated
identity and username; CLA version and revision; acceptance timestamp;
relevant pull-request identifiers; and a separate cross-border-consent record.
The project does not request a current email address or a re-entered GitHub
username as a custom field. The service providers may process other account or
technical information under their own notices.

项目配置限于法定姓名、经 GitHub 验证的身份和用户名、CLA 版本与修订、签署时间、
相关 Pull Request 标识及单独的境外处理同意记录。项目不要求将当前邮箱或重复手填的
GitHub 用户名作为自定义字段。服务提供方仍可能依其自身告知处理其他账户或技术信息。

## Overseas recipient and processing boundary / 境外接收方与处理边界

The overseas service is CLA Assistant, provided by SAP. Its current public
materials state that hosted signer data is stored using Microsoft Azure
infrastructure in Europe. Actual infrastructure and processing boundaries are
subject to the provider's current public statements; this assessment does not
promise that all processing remains exclusively within the European Union.
See the [CLA Assistant source repository](https://github.com/cla-assistant/cla-assistant)
and [SAP's CLA Assistant privacy statement](https://gist.github.com/CLAassistant/3a73e4cd729c9d0a6e30).

境外服务为 SAP 提供的 CLA Assistant。其当前公开资料说明托管签署数据使用位于欧洲的
Microsoft Azure 基础设施。实际基础设施和处理边界以服务提供方当时的公开声明为准；
本评估不承诺所有处理仅限欧盟境内。参见
[CLA Assistant 源仓库](https://github.com/cla-assistant/cla-assistant)及
[SAP 的 CLA Assistant 隐私声明](https://gist.github.com/CLAassistant/3a73e4cd729c9d0a6e30)。

## Necessity / 必要性

A pull-request checkbox alone does not produce a reliable, authenticated, and
versioned signature record. Compared with building and operating a separate
identity and signature system, the planned hosted workflow requires less
project-requested data and avoids an additional project-operated personal-data
database while preserving an auditable acceptance record.

单独的 Pull Request 复选框不足以形成可靠、经身份验证且带版本的签署记录。与自建和
运营实名签署系统相比，拟采用的托管流程要求的项目字段更少，也避免新增由项目运营的
个人信息数据库，同时仍可保留可审计的接受记录。

## Risks and mitigations / 风险与缓解措施

Identified risks include a third-party service breach; linkage between GitHub
identity and legal name; overseas processing; provider or infrastructure
changes; and additional storage copies created by maintainer exports.

已识别风险包括第三方服务数据泄露、GitHub 身份与法定姓名的关联、境外处理、服务方或
基础设施变化，以及维护者导出记录后产生额外存储副本。

Mitigations are: minimum project fields; no project-requested email field; a
published privacy notice; a separate required cross-border confirmation;
non-publication of legal names and signature data; exports only when necessary;
access controls for every export; no long-lived duplicate local database unless
necessary; and professional legal advice if risk, scale, data categories,
commercial reliance, or dispute use materially increases.

缓解措施包括：仅配置最少字段；不额外要求邮箱；发布隐私说明；设置独立且必填的境外
处理确认；不公开实名和签署数据；仅在必要时导出；对每份导出实施访问控制；非必要不
建立长期重复的本地数据库；风险、规模、数据类型、商业依赖或争议用途实质增加时取得
专业法律意见。

## Conclusion and review trigger / 结论与复评触发条件

Expected volume is small, data categories are limited, and purposes are
specific. With the stated minimization, notice, separate confirmation, and
access controls, the present risk is considered acceptable for the planned
workflow. Reassess before activation if the actual configuration differs, and
again whenever the data categories, scale, provider, infrastructure, or
processing purpose changes materially.

预计处理规模较小、信息种类有限、目的明确。在落实上述最小化、告知、单独确认和访问
控制后，当前风险对拟定流程而言可以接受。正式启用前，如实际配置与本记录不一致，应
先重新评估；信息种类、规模、服务方、基础设施或处理目的发生重大变化时亦须复评。

## Retention / 保留

Retain this assessment and the related processing records for at least three
years, or longer where applicable law requires. Signature records themselves
remain subject to the necessity-based retention described in the
[CLA Signer Privacy Notice](./CLA_PRIVACY.md).

本评估及相关处理记录至少保留三年；适用法律要求更长期限的，从其规定。签署记录本身
仍按 [CLA 签署者隐私说明](./CLA_PRIVACY.md) 所述的必要性标准管理。
