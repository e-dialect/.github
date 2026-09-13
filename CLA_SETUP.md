# CLA Assistant Setup

Status: **documentation prepared; activation waits for the governance PR to be
manually merged.**

## Agreement identity

- Agreement: `ICLA.md`
- Version: `1.0`
- Merged Git commit: pending manual merge
- SHA-256 of the merged `ICLA.md`: pending manual merge
- Public Gist URL and revision: pending manual merge

The public Gist must contain bytes identical to the merged `ICLA.md`. Record
both the repository commit and the Gist revision before enabling checks.

## CLA Assistant configuration

- Organization: `e-dialect`
- Service: <https://cla-assistant.io/>
- GitHub App: <https://github.com/apps/cla-assistant>
- Required custom fields (minimum):
  - legal name;
  - current email address;
- Obtain the GitHub username from the GitHub-authenticated signature record;
  do not ask the signer to type it again as a custom field.
- If professional legal review concludes that email is not required, remove it
  rather than collecting redundant personal data.
- A material ICLA change requires acceptance of the new version.
- CCLA signatures are reviewed and recorded manually.
- Do not treat a pull-request checkbox, commit, or PR creation as acceptance.
- Configure this repository's [`CLA_PRIVACY.md`](./CLA_PRIVACY.md) as the
  project Privacy Policy URL.
- CLA Assistant’s hosted service states that signer data is stored in Microsoft
  Azure infrastructure in Europe. Maintainers should periodically export the
  signer record only for access-controlled rights-chain and audit retention.

## Repositories to enable

### Cohort 1

1. `.github`
2. `xiangsheng-box`
3. `wanyu-proofreader`
4. `edialect.top`
5. `hinghwa-chat`
6. `hinghwa-dict-backend`
7. `hinghwa-dict-web`
8. `hinghwa-dict-uni-app`

### Cohort 2 — only after path-level licensing is reviewed

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
