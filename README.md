# The Autheo Stack

A single static, public page showing how Marketplace provider orchestration supplies Layer 0 DevHub hosting, while a distinct proposed Layer 1 handles verification/settlement; MCP agent-facing tools, a reference agent trust environment, the AssetTrack reefer pilot and the non-custodial RWA stack (tokenization, DEX, cross-chain interop with Lumenco physical attestation) complete the picture. No login, secrets, API, build process, tracking scripts or external fonts.

## Run and deploy

Open `index.html` directly, or serve the directory:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Deploy the repository root as a **static site**, with `index.html` as the entry point. There are no build commands, environment variables or backend requirements. On a static host, upload `index.html`, `styles.css`, `stack-map.svg`, and `favicon.svg` together. GitHub Pages works from the root of `main` after it is enabled in repository settings; a `.nojekyll` file is included to prevent Jekyll processing.

The SVG is an original editable vector. Its `<title>` and `<desc>` describe the concept; the HTML immediately below it gives a keyboard-accessible text equivalent. The page supports narrow screens and reduced-motion preferences.

## Scope and evidence

This is an **architecture narrative**, not an integration dashboard or live chain explorer:

| Piece | Source | Current boundary |
| --- | --- | --- |
| Layer 0 / DevHub | [L0_devhub_deploy](https://github.com/autheo-os/L0_devhub_deploy) | Hosting platform; deployment configuration is separate from this site. |
| Marketplace provider orchestration | autheo_marketplace_deploy (private repository) | Provider profiles, offers, terms and reporting. DevHub remains the scheduler; verified bindings, preview listings and paid capacity are **not** asserted live. |
| Layer 1 verification and token settlement | [MCP chain reads](https://github.com/autheo-os/autheo-MCP) and [AssetTrack's optional anchoring](https://autheo-asset-track.shadw.app/) | Integration vision here; this site does not sign, anchor or settle transactions. |
| RWA stack (tokenization + DEX + interop, Lumenco attestation) | [TaaS plan](https://thothdivision.github.io/autheo-taas-plan/) · development repo private | In development; non-custodial (users hold keys); not live, no assets issued. |
| MCP tools | [autheo-MCP](https://github.com/autheo-os/autheo-MCP) | Configured prototype; not automatically connected to a live service. |
| Agent trust environment | [autheo-agent-environment](https://github.com/SolutionsAsService/autheo-agent-environment) | Local reference simulation with signed passports/mandates, not a production DID registry or wallet. |
| AssetTrack | [AssetTrack concept](https://autheo-asset-track.shadw.app/) (repository private) | Owner-scoped reefer pilot; sample `did:` strings are illustrative labels, not registered identities or live telemetry. |

Marketplace coordinates the provider side while DevHub owns deployment and placement. The diagram's arrows show **intended** relationships, not a claim that these repositories are currently integrated. Layer 1 is a separate proof rail, not a Marketplace scheduler or payment command. Real settlements require verified signed proofs, an approved contract, exception gating and controlled funds. This public site deliberately cannot perform any such action.

## Ecosystem plan

The page also carries the ecosystem plan: how the agent environment plugs into the RWA stack (agents quote and build orders under mandates, humans sign, receipts link into the audit chain), a cross-project dependency map and a staged roadmap where every stage has an exit test and a stop condition. Stage numbers map to the [TaaS build plan](https://github.com/ThothDivision/autheo-taas-plan/blob/main/docs/BUILD-PLAN.md) milestones and the [DEX roadmap](https://github.com/ThothDivision/autheo-dex-plan/blob/main/docs/ROADMAP.md) phases; the private build repository is mentioned only at a high level. `PLANNING-LOG.md` records the P-DADA / PMDAA planning run (panel rounds R0–R5).

See `DESIGN-LOG.md` for the Adaptive DADA design process, critiques and evidence.
