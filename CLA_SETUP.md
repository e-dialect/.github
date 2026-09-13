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
- Required custom fields:
  - legal name;
  - current email address;
  - current GitHub username.
- A material ICLA change requires acceptance of the new version.
- CCLA signatures are reviewed and recorded manually.
- Do not treat a pull-request checkbox, commit, or PR creation as acceptance.
- CLA Assistant’s hosted service states that signer data is stored in Microsoft
  Azure infrastructure in Europe. Maintainers should periodically export the
  signer record for access-controlled audit retention.

## Repositories to enable

1. `.github`
2. `xiangsheng-box`
3. `hinghwa-dict-backend`
4. `hinghwa-dict-web`
5. `hinghwa-dict-uni-app`
6. `hinghwa-chat`
7. `wanyu-proofreader`
8. `edialect.top`
9. `hinghwa_semantic_retrieval`
10. `ipa_tts_minimal`
11. `Voice_Whisper`
12. `quick-start`

Do not enable this CLA for forks, private or archived repositories, legacy
repositories, or `code-contributing-practice`.
