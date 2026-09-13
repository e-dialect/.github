# Asset and Data Licensing Policy

Software licenses and the e-dialect code CLA do not create a universal license
for datasets, recordings, models, media, personal data, or brands. Each asset
must have documented provenance, authority, consent where applicable, and an
express license or other permitted-use basis before publication or reuse.

| Asset category | Automatically covered by a software `LICENSE`? | Required record or terms |
|---|---:|---|
| Source code | Yes, according to repository/path scope | Repository or path `LICENSE`; CLA where enabled |
| Software documentation | Only according to repository/path scope | CC or applicable software/documentation license |
| Dictionary or lexical content | No | Separate provenance and data license or permission |
| Corpus | No | Separate corpus/data license |
| User recording | No | Contributor and speaker consent plus data terms |
| Historical media | No | Original media authorization and attribution |
| TTS voice sample | No | Express voice-synthesis authorization and consent |
| Model weights | No | Separate model license and upstream conditions |
| Generated audio or data | No | Case-specific review of model, sources, contract, and applicable law |
| Personal or biometric data | No | Privacy notice, lawful basis, consent where required, and access controls |
| Logo, name, or brand asset | No | Trademark and brand policy or express permission |

No asset should be described as “open” solely because it is stored in a public
code repository. If its terms are missing or its provenance is unresolved, no
additional permission to copy, train on, distribute, synthesize, or commercially
reuse it is granted.

In particular, an ICLA for contributing code is **not** an agreement to
contribute a person's voice, recording, corpus, dictionary content, or other
data. Those contributions require a separate, purpose-specific written
agreement. This policy deliberately does not create a universal data, corpus,
recording, or voice license.

Third-party license and attribution files must remain with the relevant path.
Privacy, consent, publicity/personality, biometric, copyright, database,
contract, and trademark requirements may apply independently of an open-source
license.

## Current operational rule

Until e-dialect publishes a separate contribution or license agreement for the
relevant asset category, an ordinary software pull request must not directly
add the asset itself when it is a dataset, corpus, dictionary or lexical
content, fieldwork material, recording, speaker or voice sample, biometric or
personal data, linguistic annotation submitted as a dataset, model weight, or
generated media or data intended as a reusable dataset.

Contributors may instead submit source leads, links to public sources,
provenance information, or code for processing, proofreading, conversion, and
quality checks. They may also contact maintainers to discuss a contribution
that needs a separate asset agreement. Uploading material to GitHub or opening
a pull request must not be interpreted as granting rights in that material.

An asset whose provenance or licensing authority has not been reviewed must
not be incorporated into an official dataset or product data pipeline merely
because it came from a community contribution.

---

# 资产与数据许可证政策

软件许可证和 e-dialect 代码 CLA 不会为数据集、录音、模型、媒体、个人数据或品牌
建立万能许可。每项资产在发布或复用前，都必须记录来源、授权依据、必要的同意，以及
明确许可证或其他合法使用依据。

| 资产类别 | 软件 `LICENSE` 自动覆盖？ | 所需记录或条款 |
|---|---:|---|
| 源代码 | 是，按仓库或路径范围 | 仓库/路径 `LICENSE`；适用时另有 CLA |
| 软件文档 | 仅按仓库或路径范围 | CC 或适用的软件/文档许可证 |
| 词典或词汇内容 | 否 | 独立来源记录及数据许可证或授权 |
| 语料库 | 否 | 独立语料/数据许可证 |
| 用户录音 | 否 | 贡献者与说话人同意，加数据条款 |
| 历史媒体 | 否 | 原媒体授权及署名 |
| TTS 声音样本 | 否 | 明确的语音合成授权与同意 |
| 模型权重 | 否 | 独立模型许可证及上游条件 |
| 生成音频或数据 | 否 | 按模型、来源、合同和适用法律逐案判断 |
| 个人或生物识别数据 | 否 | 隐私说明、合法依据、必要同意及访问控制 |
| Logo、名称或品牌资产 | 否 | 商标/品牌政策或明确授权 |

资产不能仅因存放在公开代码仓库就被描述为“开放”。若缺少条款或来源尚未解决，不授予
复制、训练、分发、合成或商业复用的额外许可。

尤其需要明确：**贡献代码的 ICLA 不能代替贡献自己的声音、录音、语料、词典内容或
其他数据的授权**。这些贡献必须另行使用针对具体目的的书面协议。本文有意不创设万能
的数据、语料、录音或声音许可证。

第三方许可证和署名文件必须与对应路径一同保留。隐私、同意、人格/公开权、生物识别、
版权、数据库、合同和商标要求可能独立于开源许可证继续适用。

## 当前执行规则

在 e-dialect 针对相关资产发布单独的贡献或授权协议以前，普通软件 Pull Request 不得
直接新增以下资产本体：数据集、语料库、词典或词汇内容、田野材料、录音、说话人或
声音样本、生物识别或个人数据、作为数据集提交的语言学标注、模型权重，以及拟作为
可复用数据集的生成媒体或数据。

贡献者可以提交数据来源线索、公开来源链接、来源与权利信息，以及数据处理、校对、
转换和质量检查代码；也可以联系维护者讨论需要单独资产协议的贡献。将材料上传到
GitHub 或创建 Pull Request，不得被解释为已经授予该材料的相关权利。

尚未完成来源或授权依据审查的资产，不得仅因来自社区贡献就自动并入正式数据集或
产品数据管线。
