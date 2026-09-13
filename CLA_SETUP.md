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

After the first external contributor signs Version 1.0, do not make cosmetic,
formatting, or metadata-only edits to that version's Gist. Any material change
must use a new CLA version and require explicit acceptance for later
Contributions.

## Default individual-contributor flow

The normal flow must stay minimal:

1. The individual opens a pull request.
2. CLA Assistant prompts the individual on the first Contribution covered by
   the current ICLA version.
3. The individual explicitly accepts that ICLA version.
4. The individual normally takes no further action for later Contributions
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
5. the covered accounts are added to the applicable CLA exemption or
   allowlist; and
6. a test pull request confirms that a covered account is not incorrectly
   required to sign the individual ICLA.

The minimum private record is the Corporate Contributor legal name, CCLA
version, GitHub username, effective date, and revoked date when applicable. No
database, dedicated administration service, public employee registry, or
public names and email list is required. An exemption records coverage but
creates no rights; the countersigned CCLA is the source of the license.

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

## Multi-author Contributions

A passing CLA check is necessary but does not replace review of real
authorship. If a commit or pull request includes a human `Co-authored-by:`
trailer, or otherwise identifies another material author, maintainers must
confirm that each such author is covered by the ICLA, a countersigned CCLA, or
another valid rights basis. Bots may use a narrow allowlist. Students and other
individual contributors must not receive a blanket exemption merely because
they belong to a team.
