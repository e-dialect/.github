# CLA Assistant Setup

Status: **ICLA Version 1.0 is active for `e-dialect/.github`; expansion to
other repositories remains pending under issue #6.**

## Agreement identity

- Agreement: `ICLA.md`
- Version: `1.0`
- Merged Git commit:
  [`26f24cb518d6bc03d26b8f27c64e172ff3988d33`](https://github.com/e-dialect/.github/commit/26f24cb518d6bc03d26b8f27c64e172ff3988d33)
- SHA-256 of the merged `ICLA.md`:
  `445bd124d129f75a377629fecbcd58c14aa25c78acefca7c877d3a9e46547f85`
- Public Gist URL:
  <https://gist.github.com/lin594/e7aad6aea670fb1075a294f1269e58ae>
- Gist revision: `b41fb7e4f5a53d57092b133757bdc23c92a417a0`

The public Gist must contain bytes identical to the merged `ICLA.md`. Record
both the repository commit and the Gist revision before enabling checks.

Before activating another repository, confirm that
[`CLA_PIPIA.md`](./CLA_PIPIA.md) still matches the actual provider, metadata,
privacy URL, data flow, and retention practice. Reassess and update that record
first if the production configuration materially differs.

After the first external contributor signs Version 1.0, do not make cosmetic,
formatting, or metadata-only edits to that version's Gist. Any material change
must use a new CLA version and require explicit acceptance for later
Contributions.

## Default individual-contributor flow

The normal flow must stay minimal:

1. The individual opens a pull request.
2. CLA Assistant prompts the individual on the first Contribution covered by
   the current ICLA version.
3. The individual separately confirms the cross-border processing described in
   the project Privacy Notice.
4. The individual explicitly accepts that ICLA version. The cross-border
   confirmation is a separate required boolean and is not itself ICLA
   acceptance.
5. The individual normally takes no further action for later Contributions
   covered by the same version.

The GitHub username comes from the GitHub-authenticated signature record and
must not be requested again as a custom field.

## Low-frequency corporate-contributor flow

Do not deploy a standing enterprise CLA system. Only when a company or other
organization actually contributes:

1. a maintainer sends the CCLA;
2. the Corporate Contributor and Project Manager both sign it;
3. the Corporate Contributor supplies its Authorized Contributors' GitHub
   usernames;
4. the maintainer records only the minimum private coverage information;
5. the covered accounts' exact GitHub usernames are added to CLA Assistant's
   user allowlist through `allowListPattern`;
6. when an account ceases to be an Authorized Contributor, it is removed from
   the exemption for future Contributions without changing the status of
   Contributions submitted and accepted during valid CCLA coverage; and
7. a test pull request confirms that a covered account is not incorrectly
   required to sign the individual ICLA.

The minimum private record is the Corporate Contributor legal name, CCLA
version, GitHub username, effective date, and revoked date when applicable. No
database, dedicated administration service, public employee registry, or
public names and email list is required. An exemption records coverage but
creates no rights; the countersigned CCLA is the source of the license.

Use exact usernames and do not use broad wildcard patterns for CCLA-covered
employees, students, or other humans. Document bot allowlist entries separately
from CCLA allowlist entries. CLA Assistant's signature Import function **must
not** be used to represent CCLA coverage or create an apparent ICLA signature
for a person who did not sign the ICLA.

## CLA Assistant configuration

- Organization: `e-dialect`
- Service: <https://cla-assistant.io/>
- GitHub App: <https://github.com/apps/cla-assistant>
- Before installation, restrict GitHub App installation in the organization's
  member-privilege settings to Organization Owners.
- Required project metadata fields:
  - legal name as the only project-requested text custom field;
  - a separate required boolean confirming the cross-border processing
    described in the project Privacy Notice.
- Obtain the GitHub username from the GitHub-authenticated signature record;
  do not ask the signer to type it again as a custom field.
- Do not request a current email address as an e-dialect custom field. This
  does not imply that GitHub, CLA Assistant, or SAP never processes an account
  email under its own terms and notices.
- A material ICLA change requires acceptance of the new version.
- CCLA signatures are reviewed and recorded manually.
- Do not treat a pull-request checkbox, commit, or PR creation as acceptance.
- Configure
  <https://github.com/e-dialect/.github/blob/main/CLA_PRIVACY.md> as the project
  Privacy Policy URL.
- CLA Assistant’s hosted service states that signer data is stored in Microsoft
  Azure infrastructure in Europe. Maintainers should periodically export the
  signer record only for access-controlled rights-chain and audit retention.

The Gist file named `metadata` must follow CLA Assistant's current
[`custom-fields-schema.json`](https://github.com/cla-assistant/cla-assistant/blob/main/custom-fields-schema.json).
The current schema supports a required `boolean`. Use this minimum configuration
after the final ICLA Gist is created:

```json
{
  "legalName": {
    "title": "Legal name / 法定姓名",
    "description": "Enter your legal name for the ICLA signature record. / 请填写用于 ICLA 签署记录的法定姓名。",
    "type": "string",
    "required": true
  },
  "crossBorderConsent": {
    "title": "I separately consent to the cross-border processing of my CLA signature information as described in the e-dialect CLA Privacy Notice. / 我已阅读 e-dialect CLA 隐私说明，并单独同意按其中说明将我的 CLA 签署相关个人信息提供至境外服务进行处理。",
    "description": "This confirmation is separate from accepting the ICLA. / 此确认独立于对 ICLA 的接受。",
    "type": "boolean",
    "required": true
  }
}
```

Before production activation, validate the final metadata against the then
current schema and use a test account to confirm that the bilingual field is
displayed, leaving it unchecked blocks completion, checking it is recorded,
and the configured Privacy Policy URL opens the published notice. The required
boolean is shown to every signer in the enabled workflow so that a signer in
mainland China cannot complete the flow without the separate confirmation.

## Repositories to enable

Merging the organization governance pull request does **not** enable CLA checks
for every repository. Before enabling any repository, confirm that its root
license, path-level third-party license boundary, and data or asset boundary
have each been completed, reviewed, and merged.

The rollout order for each repository is:

1. merge organization governance;
2. merge that repository's license and boundary pull request;
3. test CLA behavior;
4. record the real check-run name; and
5. add that exact check to branch protection or a ruleset.

### Cohort 1 — enable one repository at a time after its boundaries are merged

1. `.github`
2. `xiangsheng-box`
3. `wanyu-proofreader`
4. `edialect.top`
5. `hinghwa-chat`
6. `hinghwa-dict-backend`
7. `hinghwa-dict-web`
8. `hinghwa-dict-uni-app`

### Cohort 2 — only after path-level licensing is reviewed and merged

1. `hinghwa_semantic_retrieval`
2. `ipa_tts_minimal`
3. `Voice_Whisper`
4. `quick-start`

Do not enable this CLA for `code-contributing-practice`, `hinghwa-ime`,
`hinghwa-RAG`, `hinghwa-dict-basic-service`, `hinghwa-dict-mp-weixin`, or any
private/archived legacy repository. Select repositories explicitly; never use
“All repositories”.

## Required check rollout

1. Enable the selected repository on a test pull request.
2. Record the actual check-run name emitted by CLA Assistant.
3. Confirm a signed test contribution passes and an unsigned one is blocked.
4. Only then add that exact check name to branch protection or a ruleset.

Do not guess the check name. Bot accounts may use a narrow allowlist; ordinary
student accounts must not be exempted.

## Activation ledger

This table establishes when each repository became a Covered Repository for a
specific CLA version. Add one row immediately after each repository is enabled.
Do not record contributor personal information. Use an unambiguous date and
time for `Enabled at`, the commit containing the formally merged ICLA, the real
Gist revision, and the check name observed in the test pull request.

| Repository | CLA version | Enabled at | ICLA repository commit | Gist revision | CLA check name |
|---|---|---|---|---|---|
| `e-dialect/.github` | `1.0` | `2026-09-15T11:09:51Z` | `26f24cb518d6bc03d26b8f27c64e172ff3988d33` | `b41fb7e4f5a53d57092b133757bdc23c92a417a0` | `license/cla` |

## Multi-author Contributions

A passing CLA check is necessary but does not replace review of real
authorship. If a commit or pull request includes a human `Co-authored-by:`
trailer, or otherwise identifies another material author, maintainers must
confirm that each such author is covered by the ICLA, a countersigned CCLA, or
another valid rights basis. Bots may use a narrow allowlist. Students and other
individual contributors must not receive a blanket exemption merely because
they belong to a team.
