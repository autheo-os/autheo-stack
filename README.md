# The Autheo Stack

A single static, public page showing how Layer 0 hosting, proposed Layer 1 verification/settlement, MCP agent-facing tools, a reference agent trust environment, and the AssetTrack reefer pilot fit together. No login, secrets, API, build process, tracking scripts or external fonts.

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
| Layer 1 verification and token settlement | [MCP chain reads](https://github.com/autheo-os/autheo-MCP) and [AssetTrack's optional anchoring](https://github.com/ThothDivision/autheo-asset-track) | Integration vision here; this site does not sign, anchor or settle transactions. |
| MCP tools | [autheo-MCP](https://github.com/autheo-os/autheo-MCP) | Configured prototype; not automatically connected to a live service. |
| Agent trust environment | [autheo-agent-environment](https://github.com/autheo-os/autheo-agent-environment) | Local reference simulation with signed passports/mandates, not a production DID registry or wallet. |
| AssetTrack | [autheo-asset-track](https://github.com/ThothDivision/autheo-asset-track) | Owner-scoped reefer pilot; sample `did:` strings are illustrative labels, not registered identities or live telemetry. |

The arrows show intended relationships, **not** a claim that these repositories are currently integrated. Real settlements require verified signed proofs, an approved contract, exception gating and controlled funds. This public site deliberately cannot perform any such action.

See `DESIGN-LOG.md` for the Adaptive DADA design process, critiques and evidence.
