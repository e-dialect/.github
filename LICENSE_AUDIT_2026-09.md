# e-dialect License Audit — 2026-09

Audit baseline: **2026-09-13**. Repository metadata and open-item counts were
captured immediately before lifecycle changes. “PARTIAL” means open-source
licensing may proceed on the confirmed authority, while a complete auditable
chain for alternative commercial relicensing still depends on contributor
records or back-signatures.

| Repository | Lifecycle | Current / target license | Third-party code | CLA | Commercial relicensing | Action and follow-up |
|---|---|---|---|---|---|---|
| `.github` | Active, public | None → CC-BY-4.0 | No material indication | Yes | Not applicable | Governance PR; ICLA/CCLA v1.0 and CLA setup |
| `chuyan-hinghwa-dict-backend` | Archived, private | No declared license | Not audited | No | Not applicable | Audit only |
| `chuyan-hinghwa-dict-web` | Archived, private | No declared license | Not audited | No | Not applicable | Audit only |
| `code-contributing-practice` | Active public fork | GPL-2.0 retained | Yes, upstream fork | No | No / upstream-limited | Sole public Git/GitHub practice entry; no relicensing |
| `django-template` | Private, archived during this pass | No declared license | Not audited | No | Not applicable | Future deletion candidate tracked in `.github#4`; no deletion authorized |
| `edialect.top` | Active, public | None → AGPL-3.0-only | Normal dependencies; provenance reviewed | Yes | PARTIAL | Repository license PR |
| `Git-Practice` | Private, archived during this pass | No declared license | Not audited | No | Not applicable | 11 issues and 3 PRs notified and closed; replaced by `code-contributing-practice` |
| `hinghwa-chat` | Active, public | AGPL-3.0 retained; clarified as AGPL-3.0-only | Normal dependencies | Yes | PARTIAL | Add repository licensing boundary |
| `hinghwa-dict-backend` | Active, public | AGPL-3.0 retained; clarified as AGPL-3.0-only | Normal dependencies | Yes | PARTIAL | Add repository licensing boundary |
| `hinghwa-dict-basic-service` | Legacy, public | GPL-3.0 retained | Not fully audited | No | Not assessed (legacy) | No relicensing; pending retirement |
| `hinghwa-dict-mp-weixin` | Archived, public | No declared license | Not audited | No | Not applicable | Audit only |
| `hinghwa-dict-uni-app` | Active, public | AGPL-3.0 retained; clarified as AGPL-3.0-only | Normal dependencies | Yes | PARTIAL | Add repository licensing boundary |
| `hinghwa-dict-v2` | Private, archived during this pass | No declared license | Not audited | No | Not applicable | Replaced by [`xiangsheng-box`](https://github.com/e-dialect/xiangsheng-box); no relicensing or deletion |
| `hinghwa-dict-web` | Active, public | AGPL-3.0 retained; clarified as AGPL-3.0-only | Normal dependencies | Yes | PARTIAL | Add repository licensing boundary |
| `hinghwa-ime` | Active public fork | MPL-2.0 retained | Yes, upstream fork | No | No / upstream-limited | Add exception and upstream boundary; no relicensing |
| `hinghwa-RAG` | Active public fork | No upstream license; no open-source grant inferred | Yes, upstream fork | No | No / upstream-limited | Add restrictive boundary; request upstream decision from `@Tingwuren` |
| `hinghwa_semantic_retrieval` | Active, public | Path-partitioned AGPL-3.0-only / third-party terms / unlicensed assets | Model, data and generated artifacts | Yes | PARTIAL for original code | Add `LICENSES`, boundary and notices; assets excluded |
| `ipa_tts_minimal` | Active, public | Current tree AGPL-3.0-only; historical DiaMoE MIT | Historical upstream source | Yes | PARTIAL for current tree | Preserve DiaMoE MIT copyright and revision boundary |
| `quick-start` | Active, public | None → CC-BY-SA-4.0 | No material indication | Yes | Not applicable | Documentation license PR |
| `Voice_Whisper` | Active, public | Multi-origin; AGPL-3.0-only only for identifiable original glue | Multiple bundled upstream trees | Yes for original glue | PARTIAL / upstream-limited | Path-level licensing and third-party notices; media excluded |
| `wanyu-proofreader` | Active, public | None → AGPL-3.0-only | Bundled fonts/PDF.js assets under retained terms | Yes | PARTIAL | Root license and boundary PR |
| `xiangsheng-box` | Active, public | AGPL-3.0 retained; clarified as AGPL-3.0-only | Normal dependencies and separately governed data | Yes | PARTIAL | Licensing clarification; official successor to `hinghwa-dict-v2` |

## Confirmed licensing principles

- AGPL allows commercial use subject to its terms. Alternative commercial
  licensing is an optional parallel license for users who cannot or do not wish
  to comply with AGPL; it is not a commercial-use surcharge.
- No repository-wide policy overrides third-party licenses or copyright.
- Software licenses do not automatically cover datasets, corpora, dictionary
  content, recordings, model weights, generated artifacts, trademarks, or logos.
- Existing public open-source releases retain the rights already granted.

## Pull requests and governance issues

PR links will be updated on this branch after each repository-specific PR is
opened. Lifecycle issue: [`django-template` deletion candidate #4](https://github.com/e-dialect/.github/issues/4).
