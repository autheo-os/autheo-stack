# PLANNING-LOG — Autheo ecosystem plan (autheo-stack)

Run: 2026-10-13 · Skill: PMDAA Plan mode (= P-DADA contract) · Mode: **Vision** · Page: `index.html` (public, hosted at autheo-stack.shadw.app)
Tools: OpenClaw exec + gh CLI (live repo/CI checks), PMDAA `portfolio.py` (portfolio ledger refresh), 7 critic subagents per round
(one per reference), headless Chrome (puppeteer-core) renders at 1440 px and 390 px. No graph renderer was needed; the Mermaid
graphs were followed by label.

## 1. Traversal Plan

- **Mode: Vision.** Readers are partners, investors and builders deciding whether to back or join the Autheo ecosystem; the build
  plan of record lives in the TaaS plan (Execution mode), this page must persuade and stay true.
- **Reader → decision:** partner: "where do we come in, and when?"; investor: "is there a strategy, and what is real?";
  builder: "what do I depend on, and what is the next test?".
- **Governing criterion:** Kernel of Good Strategy (diagnosis, guiding policy, coherent action), and every checkable claim true or labelled.
- **Hard limits:** the private RWA build repository is mentioned only at a high level (no internals); no claim that any
  integration is live; not an offer of securities; keep the inherited DADA design (no restructure of map, SVG or cards).
- **Seed (exact labels, references/planning-graph.md):** `Kernel of Good Strategy: diagnosis, guiding policy, coherent action (Rumelt, Good Strategy Bad Strategy)`;
  `Code is law: rules enforced by architecture (Lessig, Code and Other Laws of Cyberspace)`; `STRIDE threat modeling (Shostack, Threat Modeling)`;
  `Reference class forecasting; think slow, act fast (Flyvbjerg, How Big Things Get Done)`; dotted counterpoint
  `Bad strategy: fluff, goals mistaken for strategy (Rumelt)` (kernel -.-> badstrat).
- **Inputs read:** inherited `index.html`, `README.md`, `DESIGN-LOG.md`, `stack-map.svg`; TaaS `BUILD-PLAN.md` (milestones, outside view),
  `DECISIONS-AND-RISKS.md` (D-04, D-11), `NORTH-STAR.md` ("the agent never signs"); DEX `ROADMAP.md` (phases 0–5); agent environment
  `README.md` and `docs/ROADMAP.md` (phases 0, 0.2 done; A–G); RWA build README (private; used for status only). Live checks: gh repo
  view + run list for all 9 portfolio repos (see `~/.openclaw/workspace/portfolio/autheo/PORTFOLIO.yaml`, private), curl of every outbound link.

### Frontier (final state)

| Candidate | Reached via (edge, direction) | From anchor | Status |
|---|---|---|---|
| RWA card states planned capabilities in present tense | premortem -.-> kernel (attack the boldest bet) | premortem | TAKEN (M1) |
| No diagnosis / guiding policy on the page | kernel -.-> badstrat | kernel | TAKEN (M2) |
| Agent ↔ DEX/RWA boundary undefined (who signs) | policycode --> licence; crit_shostack --> stride | policycode, stride | TAKEN (M3) |
| STRIDE at the agent → order boundary | privacy --> stride --> register | stride | TAKEN (M3, M7, M9) |
| Cross-project dependency map + critical path | brooks --> refclass --> register; conway -.-> brooks | refclass | TAKEN (M4) |
| Staged roadmap with exit tests | dod --> exitaudit; walking --> dod | dod | TAKEN (M5) |
| Outside view for the roadmap | brooks --> refclass | refclass | TAKEN (M6, M8) |
| Holder protections (freeze, appeal, liability) | crit_omitted --> licence | licence | TAKEN (M7) |
| Dead / private links on a public page | claimaudit (Build: links resolve) | claimaudit | TAKEN (M1) |
| Replace h1 headline with the bet | pyramid --> krug | pyramid | DEFERRED (overrule O1) |
| Named owners per stage on the public page | adr --> decaudit | decaudit | DEFERRED (overrule O2: owners not public yet; held in the private ledger) |
| Renumber layers / merge repeated caveats | krug --> dadadesign | krug | DEFERRED (overrule O3: restructure out of scope) |
| Per-route bridge trust, jurisdictions | stride; licence | stride | DEFERRED (O4: Stage 6 / counsel item on the page) |
| One status vocabulary across badges, SVG and table | consistency | consistency | DEFERRED (minor; next site edit; recorded in the ledger) |

## 2. Decision Records

### Move M1: Stop present-tense claims; fix dead links (BREAK)
- Anchor and edge: `Premortem (Gary Klein, Performing a Project Premortem)` -.->|attack the boldest bet| `Kernel of Good Strategy…`; claim audit.
- Depends on: R0 (Minto, Klein, Flyvbjerg: ANDON).
- Hypothesis: a reader can tell a promise from a working system on every card.
- Options: (a) delete the RWA card; (b) rewrite as "Planned … Today …" in place. Recommendation (b): keeps the inherited design, adds the boundary.
- Measurement: present-tense live-sounding claims about the RWA stack 4 (card, reading order, mobile map, SVG label) → 0; outbound links returning 404 to the public 2 (Marketplace, AssetTrack) → 0; links to a stale fork 1 → 0.
- Result: KEEP.

### Move M2: Diagnosis and guiding policy in the hero (KEEP-THE-RULE)
- Anchor: `Kernel of Good Strategy…` -.->|counterpoint: goals are not strategy| `Bad strategy: fluff, goals mistaken for strategy (Rumelt)`.
- Hypothesis: an investor reads the obstacle, the bet and what exists today in one paragraph.
- Options: (a) replace the h1; (b) rewrite the lead under the h1. Recommendation (b) (see O1).
- Measurement: diagnosis sentences in hero 0 → 1; guiding policy statements 0 → 1 ("Agents propose, humans sign, receipts prove") with what it rules out (3 items, `04).
- Result: KEEP (R1 Rumelt asked the obstacle to move into the hero: ADAPT in M6).

### Move M3: Section 04 — agents on the RWA stack (BREAK)
- Anchors: `Code is law: rules enforced by architecture (Lessig…)` -.->|rules in code still need a legal owner| `Regulated perimeter: who holds which licence`; `STRIDE threat modeling (Shostack, Threat Modeling)`.
- Hypothesis: a reader sees exactly where an agent's authority ends and a human signature begins, and what could go wrong there.
- Options: (a) prose paragraph; (b) 4-step flow (delegate → quote & build → human signs → settle & receipt) + STRIDE table. Recommendation (b): matches the existing flow-list design and makes threats countable.
- Measurement: STRIDE categories covered 0 → 6 (after M9); statements of "the agent never signs" 0 → 2; status label "planned / local chain only" present.
- Result: KEEP.

### Move M4: Section 05 — dependency map with critical path
- Anchor: `Reference class forecasting; think slow, act fast (Flyvbjerg…)` --> `Risk register: likelihood, impact, owner, trigger (ISO 31000)`; `Conway's law` -.-> `No silver bullet…(Brooks)`.
- Hypothesis: a builder sees what waits on what; an investor sees the single largest schedule risk.
- Options: (a) graph diagram; (b) table (piece / status / waits on / next exit test) that stacks on mobile. Recommendation (b): one source for status, readable at 390 px, no new diagram to keep in sync.
- Measurement: rows 0 → 10, each with a next exit test (10/10); critical path stated; Layer 1 testnet named as the largest schedule risk; statuses checked live against each repo's latest commit/CI.
- Result: KEEP.

### Move M5: Section 06 — staged roadmap, stages not dates (BREAK)
- Anchors: `Definition of Done and exit criteria (Schwaber and Sutherland, Scrum Guide)` --> `Exit-test audit`; `Walking skeleton (Cockburn, Crystal Clear)`.
- Hypothesis: every stage can be checked by a stranger, and Stage 2 delivers value without the testnet (modularity against the L1 risk).
- Options: (a) dated timeline; (b) six gated stages mapped to TaaS milestones and DEX/agent phases. Recommendation (b): dates are not decided; the outside view is cited instead.
- Measurement: stages with exit tests 6/6; with stop-if 2/6 → 6/6 (M8); stage names consistent with BUILD-PLAN M0–M6 and DEX phases 2–4.
- Result: KEEP.

### Move M6: R1 adaptations — tense, hero diagnosis, outside view, partner CTA
- Depends on: R1 (6 OBJECT, 1 PASS).
- Changes: hero opens with the hard problem; reading order and mobile map "planned"; SVG label "PLANNED DvP"; Lumenco "will be scanned"; Lumenco row added; header names what the table was checked against; partner call-to-action under the roadmap.
- Result: ADAPT.

### Move M7: Holder protections and open counsel items (KEEP-THE-RULE)
- Anchor: `Critic: the party the plan leaves out (Rawls…)` --> `Regulated perimeter: who holds which licence`.
- Options: (a) promise protections; (b) cite the proposed D-11 terms and list the undecided items with owner and decide-by. Recommendation (b).
- Measurement: holder-facing rules on page 0 → 1 (D-11, linked, labelled proposed); open items listed as deferred with owner (counsel) and decide-by (before Stage 4): 4; Stage 4 stop-if gates on them.
- Result: KEEP.

### Move M8: R2 adaptations — outside-view label and arithmetic, stop-if caps
- Falsification push (S4): the boldest number on the page, the schedule outside view, was recomputed. Source rows (BUILD-PLAN): inside 6+8+12+10+16+12+12 = **76**; P50 8+11+16+13+21+16+16 = **101**; P80 11+14+21+17+28+21+21 = **133** (each row rounded up before summing; 76 × 1.3 = 98.8, 76 × 1.7 = 129.2). Flyvbjerg seat flagged that the study is a cost-overrun class; the sentence now says "applied to schedule" and "the tail can be fatter". Testnet stop-if capped at M1's P80 (14 weeks).
- Result: ADAPT.

### Move M9: R2–R4 consistency — revocation in every refusal list
- STRIDE row checks latest revocations before an order is built; Stage 2 refusals and step 02 include revoked / unknown status; Stage 5 tests use after revocation; EIP-712 domain binding; DoS row (fails closed); MCP wording aligned.
- Result: ADAPT. The step-02 wording edit (Minto, R4 minor) was made after R5 and is wording-only, not re-paneled.

## 3. Panel Reports (one subagent per reference; full texts kept in the run's scratch, summarised here)

### Panel R0 premortem, inherited page (WHOLE)
| Critic (work) | Observed in the plan | Verdict | Requested change |
|---|---|---|---|
| Rumelt (Good Strategy Bad Strategy) | "Run applications. Coordinate agents. Follow assets." — goals, no diagnosis | OBJECT | Diagnosis + one guiding policy; staged roadmap from a proximate objective |
| Minto (Pyramid Principle) | RWA card present tense vs "integration vision" elsewhere | ANDON | Governing sentence; status table; boundary before example |
| Klein (premortem) | No stage, kill criterion or dependency map; who signs unstated | ANDON | Exit test + stop-if per stage; dependency map marking L1 risk |
| Krug (Don't Make Me Think) | Caveats repeated ≥ 6×; two numbering schemes | OBJECT | One status table; one numbering; plain headline; CTA |
| Shostack (Threat Modeling) | "every step is available to agents as MCP tools" | OBJECT | "Agent never signs"; decoded EIP-712; STRIDE per boundary |
| Flyvbjerg (How Big Things Get Done) | Everything funnels into L1 DvP; no reference class | ANDON | Stage 1 without L1; reference-class note; blocked-by map |
| Rawls (party left out) | Non-custodial ≠ un-freezable; no appeal/liability | OBJECT | Name freeze authority, appeal, mandate revocation; "not an offer of securities" |

### Panel R1, revised page (WHOLE)
| Critic | Observed | Verdict | Resolution |
|---|---|---|---|
| Rumelt | Reading order still "tokenizes … across chains"; obstacle only in `04 | OBJECT | ADAPT (M6) |
| Minto | No owner column; AssetTrack badge vs table wording; h1 not the bet | OBJECT | ADAPT wording (M6); OVERRULE O1, O2 |
| Klein | Stop-if only on 2/6 stages; "no testnet by M2" cannot fire | OBJECT | ADAPT (M6, M8) |
| Krug | Caveats repeated; numbering; no CTA; status vocabulary | OBJECT | ADAPT CTA (M6); OVERRULE O1, O3 |
| Shostack | No DoS row; EIP-712 domain/chainId confusion | PASS | ADAPT (M9) |
| Flyvbjerg | "reference class" mislabelled; no Lumenco row; who verified | OBJECT | ADAPT (M6, M8); OVERRULE O2 |
| Rawls | Clawback, wrong-attestation loss, appeal beyond D-11, in-mandate liability, jurisdictions | OBJECT | ADAPT (M7); OVERRULE O4 (jurisdictions = open counsel item) |

### Panel R2 (WHOLE)
| Critic | Observed | Verdict | Resolution |
|---|---|---|---|
| Rumelt | All four R1 points resolved; overrules name their trades | PASS | — |
| Minto | MCP wording mixed (minor) | PASS | ADAPT (M9) |
| Klein | Testnet stop-if fires late if M1 drags | PASS | ADAPT (M8: P80 cap) |
| Krug | Status vocabulary only partly unified (minor) | PASS | DEFERRED (Frontier) |
| Shostack | Offline verification cannot see a new revocation | PASS | ADAPT (M9) |
| Flyvbjerg | 76 × 1.3 ≠ 101; cost class applied to schedule | OBJECT | ADAPT (M8: rounding stated, relabelled) |
| Rawls | Stage 4 stop-if should include open counsel items | PASS | ADAPT (M8) |

### Panel R3 (WHOLE)
Rumelt, Minto, Klein, Krug, Shostack, Flyvbjerg: PASS (arithmetic 101/133 verified by Flyvbjerg from the rows). Rawls: OBJECT — revocation
guard has no exit test → ADAPT (M9: Stage 2 and Stage 5).

### Panel R4 (WHOLE)
All seven PASS, "none material". Minto minor: step 02 refusal list lacks "revoked" (applied after R5, wording only).

### Panel R5 (WHOLE)
All seven PASS, "none material", no requested changes.

## 4. Anchor Ledger

| Anchor (exact label) | Used in | Verdict |
|---|---|---|
| Kernel of Good Strategy: diagnosis, guiding policy, coherent action (Rumelt, Good Strategy Bad Strategy) | M2, M6 | kept |
| Bad strategy: fluff, goals mistaken for strategy (Rumelt) | M2 (dotted, applied) | adapted (hero lead) |
| Premortem (Gary Klein, Performing a Project Premortem) | R0, M1 | kept |
| Code is law: rules enforced by architecture (Lessig, Code and Other Laws of Cyberspace) | M3 | kept |
| Regulated perimeter: who holds which licence | M3, M7 | kept |
| STRIDE threat modeling (Shostack, Threat Modeling) | M3, M9 | kept |
| Risk register: likelihood, impact, owner, trigger (ISO 31000) | M4 (stop-if as triggers) | adapted (owners in private ledger) |
| Reference class forecasting; think slow, act fast (Flyvbjerg, How Big Things Get Done) | M5, M8 | adapted (cost class applied to schedule, labelled) |
| No silver bullet; adding people to a late project (Brooks, The Mythical Man-Month) | M4 (via Conway dotted edge) | visited |
| Definition of Done and exit criteria (Schwaber and Sutherland, Scrum Guide) | M5 | kept |
| Walking skeleton (Cockburn, Crystal Clear) | M5 Stage 1 | kept |
| Pyramid Principle: answer first, MECE support (Barbara Minto) | M2, O1 | adapted |
| Don't Make Me Think (Steve Krug) | M4 (mobile table), O3 | adapted |
| DADA design graph for the plan site (references/design-graph.md) | design kept; new sections reuse inherited components | kept |
| Claim audit / Decision audit / Exit-test audit / Cross-document consistency and glossary | `5 below | kept |

Dotted edges leaving used anchors (S5): kernel -.-> badstrat **applied** (M2); premortem -.-> kernel **applied** (M1);
policycode -.-> licence **applied** (M3, M7); pyramid -.-> tufte **applied** (evidence placed beside the answer: checked-against note, sourced numbers);
conway -.-> brooks **declined** (team shape is not on a public ecosystem page; held in the TaaS build plan); shapeup -.-> refclass **applied** (stages fixed by test, not time; M5);
blackswan -.-> register **applied** (the "tail can be fatter" label, M8); crit_rumelt -.-> crit_krug **applied** (seated together every round).

## 5. Audits at the final state (new and changed content)

- **Claim audit:** sourced with a link 14 (D-11 terms ×3, TaaS M0–M6 stage tests ×5, outside-view study, DEX phases ×3, agent-environment phases ×2); computed 3 (76 / 101 / 133, recomputed above); labelled planned / proposed / open 13 (6 STRIDE guards, Stage 2 test, 4 counsel items, "no agent can place a live order", "not an offer of securities"); live-verified status 10 (dependency rows, checked 2026-10-13 against latest commit and CI). Unlabelled checkable claims: 0 found.
- **Decision audit:** decided in this run 2 (guiding policy; Stage 2 needs no testnet) + 4 overrules (O1–O4) with trades named; deliberately deferred with owner and decide-by 4 (clawback; wrong-attestation and in-mandate loss; independent appeal; pilot jurisdictions → counsel, before Stage 4); open without record: 0.
- **Exit-test audit:** roadmap stages with exit test 6/6, with stop-if 6/6; dependency rows with next exit test 10/10.
- **Consistency:** stage ↔ TaaS milestone and DEX phase names match their sources; RWA status "planned / not live" consistent across card, reading order, mobile map, SVG label, dependency row and boundary; revocation consistent across step 02, STRIDE, Stage 2, Stage 5. Known residue: badge vocabulary (e.g. "Integration vision" vs table wording) — deferred.
- **Build:** HTML parses; SVG parses; headless render at 1440 px and 390 px: no horizontal overflow (scrollWidth = clientWidth), no console errors; every outbound link returned HTTP 200 in a curl check (the private Marketplace repo link now points in-page).

## 6. Stop test

- **S1** No OPEN Frontier items: met (remaining items DEFERRED with reasons).
- **S2** WHOLE round with PASS from every required critic (Rumelt, Minto, Klein, Krug + Shostack, Flyvbjerg, Rawls) and no Andon: met (R4, R5).
- **S3** Two consecutive WHOLE rounds with no ADAPT/SCRAP/REOPEN/new OPEN: met (R4, R5), with one wording-only consistency edit after R5 (step 02 "revoked"), not re-paneled — stated here.
- **S4** Falsification push: met (M8 recomputation of the outside view; label corrected).
- **S5** Every dotted edge leaving a used anchor applied or declined: met (list in `4).

**Double loop.** The criterion held, but the panel showed the planning graph has no anchor for *who can undo an action* (revocation,
freeze, appeal) — the Rawls seat carried it alone. Graph amendment proposed: add `Reversibility and recourse: revocation, freeze, appeal (Ostrom's graduated sanctions)`
under COMPLIANCE AND TRUST, with stride --> it and crit_omitted --> it.

**Carry-forward ledger.**
- The agent never signs; MCP order tools return unsigned orders (TaaS NORTH-STAR) — every agent feature must keep this.
- Layer 1 testnet is the critical-path risk; Stage 2 (agents quote, humans sign) is the first stage that needs no testnet.
- The TaaS outside view is a cost-overrun class applied to schedule: 76 / 101 / 133 weeks for M0–M6.
- Public pages may say the RWA build is a private walking skeleton on a local chain; nothing more about its internals.
- Two AssetTrack repos and two DEX dev repos exist; canonical repo decisions are pending in the private portfolio ledger.

## 7. Compliance Check

- [x] Inputs read, tools inventoried, R0 premortem run (7 subagents)
- [x] Mode, readers and criterion stated
- [x] Seed with exact labels and a dotted counterpoint; living Frontier
- [x] At least one BREAK move (M1, M3, M5); no quota used as a stopping rule
- [x] A Decision Record before each move, with options and measurements
- [x] A Panel Report per round meeting the Vision composition rule, one subagent per reference (R0–R5, 42 critic runs)
- [x] Claim, decision, exit-test and consistency audits printed at the final state
- [x] S1–S5 shown as met, with where (S3 with the stated post-R5 wording edit)
- [x] Anchor Ledger complete; final report states mode, tools, stop conditions and everything skipped

Skipped: restructuring the inherited layer numbering and repeated caveats (O3); named owners on the public page (O2); one status
vocabulary across badges and SVG (deferred). The first R0 attempt with a JSON schema failed for all seven seats and was rerun as plain text.
