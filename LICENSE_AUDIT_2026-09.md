# e-dialect License Audit — 2026-09

Audit baseline: **2026-09-13**. Repository metadata and open-item counts were
captured immediately before lifecycle changes. This report distinguishes CLA
rollout from the copyright authority needed for alternative commercial
relicensing.

Relicensing status has the following strict meanings:

- **FULL** — a complete, auditable rights chain has been confirmed for the
  stated scope;
- **PARTIAL** — open-source licensing can proceed on confirmed authority, but
  the complete rights chain for an alternative license has not been confirmed;
- **NO** — the organization does not claim alternative relicensing authority;
- **N/A** — alternative software relicensing is not applicable to this row.

No repository in this audit is marked `FULL`.

| Repository | Lifecycle | Current / target license | Third-party / data boundary | CLA enforcement | Alternative commercial relicensing | Action / follow-up |
|---|---|---|---|---|---|---|
| `.github` | Active, public | Original community documentation: CC-BY-4.0 | Future executable code needs a separate path license; assets are governed separately | Planned (Cohort 1) | N/A | Draft governance [PR #5](https://github.com/e-dialect/.github/pull/5); human R2 gate required |
| `chuyan-hinghwa-dict-backend` | Archived, private | No declared license | Not audited; no permission inferred | N/A | N/A | Audit only; do not reopen or relicense |
| `chuyan-hinghwa-dict-web` | Archived, private | No declared license | Not audited; no permission inferred | N/A | N/A | Audit only; do not reopen or relicense |
| `code-contributing-practice` | Active public fork | GPL-2.0 retained | Canonical upstream is [`lin594/code-contributing-practice`](https://github.com/lin594/code-contributing-practice); upstream ownership retained | N/A | NO | Sole public Git/GitHub practice entry; convenient organization fork only |
| `django-template` | Private, archived | No declared license | Not audited; no permission inferred | N/A | N/A | Future deletion candidate tracked in [`.github#4`](https://github.com/e-dialect/.github/issues/4); no deletion authorized |
| `edialect.top` | Active, public | Original application code: AGPL-3.0-only | Dependencies retain their terms; logos, media, corpus/content data and brands excluded | Planned (Cohort 1) | PARTIAL | Repository-specific boundary PR after governance approval |
| `Git-Practice` | Private, archived | No declared license | Historical content retained; no permission inferred | N/A | N/A | 11 issues and 3 PRs notified and closed; replaced by the canonical practice project through the e-dialect fork |
| `hinghwa-chat` | Active, public | Existing AGPL retained; current original code target AGPL-3.0-only subject to history | Dependencies retain their terms; data, media and brands excluded | Planned (Cohort 1) | PARTIAL | Preserve historical grants; add repository licensing boundary |
| `hinghwa-dict-backend` | Active, public | Existing AGPL retained; current original code target AGPL-3.0-only subject to history | Dependencies retain their terms; dictionary/data and brands excluded | Planned (Cohort 1) | PARTIAL | Preserve historical grants; add repository licensing boundary |
| `hinghwa-dict-basic-service` | Private, archived | GPL-3.0 retained | Not fully audited; historical and third-party rights retained | N/A | NO | Archive notice merged in [PR #33](https://github.com/e-dialect/hinghwa-dict-basic-service/pull/33); legacy PRs [#27](https://github.com/e-dialect/hinghwa-dict-basic-service/pull/27), [#31](https://github.com/e-dialect/hinghwa-dict-basic-service/pull/31), and [#32](https://github.com/e-dialect/hinghwa-dict-basic-service/pull/32) preserved and closed; no relicensing or deletion |
| `hinghwa-dict-mp-weixin` | Archived, public | No declared license | Not audited; no permission inferred | N/A | N/A | Audit only; do not reactivate or perform broad relicensing |
| `hinghwa-dict-uni-app` | Active, public | Existing AGPL retained; current original code target AGPL-3.0-only subject to history | Dependencies retain their terms; dictionary/data, media and brands excluded | Planned (Cohort 1) | PARTIAL | Preserve historical grants; add repository licensing boundary |
| `hinghwa-dict-v2` | Private, archived | No declared license | Not audited; no permission inferred | N/A | N/A | Replaced only by [`e-dialect/xiangsheng-box`](https://github.com/e-dialect/xiangsheng-box); no relicensing or deletion |
| `hinghwa-dict-web` | Active, public | Existing AGPL retained; current original code target AGPL-3.0-only subject to history | Dependencies retain their terms; dictionary/data, media and brands excluded | Planned (Cohort 1) | PARTIAL | Preserve historical grants; add repository licensing boundary |
| `hinghwa-ime` | Active public fork | MPL-2.0 retained | Upstream-derived code and notices remain MPL-2.0 | N/A | NO | Document fork/upstream boundary; no organization CLA over upstream work |
| `hinghwa-RAG` | Active public fork | No upstream license; no open-source grant inferred | Upstream code, prompts and data must not be reused without permission | N/A | NO | Restrictive rights notice; upstream decision requested in [issue #1](https://github.com/e-dialect/hinghwa-RAG/issues/1) |
| `hinghwa_semantic_retrieval` | Active, public | Original service code target AGPL-3.0-only; path-level exceptions | BGE/other third-party terms retained; datasets, models, indexes, caches and generated artifacts excluded | Planned after path review (Cohort 2) | PARTIAL | Add `LICENSES`, notices and asset boundaries before CLA rollout |
| `ipa_tts_minimal` | Active, public | Current original tree target AGPL-3.0-only; historical DiaMoE remains MIT | DiaMoE copyright/license and revision boundary retained; models and voice assets excluded | Planned after path review (Cohort 2) | PARTIAL | Add explicit historical and asset boundary before CLA rollout |
| `quick-start` | Active, public | Documentation: CC-BY-SA-4.0; `data-import/sql.js`: MIT | `data-import/词汇.tsv` excluded pending provenance and separate data terms | Planned after path review (Cohort 2) | N/A | Split-license dispatcher, `LICENSES/`, and `DATA_LICENSE.md`; no whole-repository CC grant |
| `Voice_Whisper` | Active, public | Original glue target AGPL-3.0-only; path-level upstream licenses retained | CosyVoice, SenseVoice, Matcha-TTS, HiFi-GAN, UVR and other upstream code retain their terms; models/media excluded | Planned after path review (Cohort 2) | PARTIAL | Complete path map and notices before CLA rollout; no whole-repository relicensing claim |
| `wanyu-proofreader` | Active, public | Original application code target AGPL-3.0-only | Bundled fonts, PDF.js and other vendor assets retain their licenses; data, documents and brands excluded | Planned (Cohort 1) | PARTIAL | Repository-specific root license and boundary PR after governance approval |
| `xiangsheng-box` | Active, public | Existing AGPL retained; current original code target AGPL-3.0-only subject to history | Dependencies retain terms; corpora, dictionary content, recordings, uploaded media, models and brands excluded | Planned (Cohort 1) | PARTIAL | Official successor to `hinghwa-dict-v2`; add path/data boundaries after governance approval |

## Confirmed licensing principles

- AGPL is an open-source license and permits commercial use subject to its
  terms. An alternative commercial license is an optional parallel license for
  users who cannot or do not wish to comply with AGPL; it is not a
  commercial-use surcharge.
- Alternative commercial licensing is available only for code Beijing Taju
  owns or for which it has obtained the necessary relicensing authority.
- No organization policy, root license, or CLA overrides third-party copyright
  and license terms.
- Software licenses and the code CLA do not automatically cover datasets,
  corpora, dictionary content, recordings, model weights, generated artifacts,
  personal data, trademarks, or logos. See
  [`ASSET_AND_DATA_POLICY.md`](./ASSET_AND_DATA_POLICY.md).
- Historical releases remain governed by their published terms; later policy
  does not revoke rights already granted to the public.

## Pull requests and governance issues

- Organization license and CLA governance: Draft [`.github PR #5`](https://github.com/e-dialect/.github/pull/5), intentionally unmerged pending `@lin594` R2 review.
- CLA installation, immutable hash, Gist revision, test PR, and real check name: [`.github issue #6`](https://github.com/e-dialect/.github/issues/6).
- Future `django-template` deletion candidate, without a due date or deletion authorization: [`.github issue #4`](https://github.com/e-dialect/.github/issues/4).
- `hinghwa-RAG` upstream license/permission request: [`hinghwa-RAG issue #1`](https://github.com/e-dialect/hinghwa-RAG/issues/1).

Repository-specific license PR links will be added only after the organization
governance draft receives its required human confirmation. Their absence here
does not imply that a license has been deployed.
