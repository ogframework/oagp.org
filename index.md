# OG

**Open Governance Framework** — Structured open governance for AI organizations.

Every meaningful AI deployment is already an organization. It has roles, hand-offs between sessions, authority boundaries, and decisions someone needs to be accountable for. Today, that structure is captive — locked inside a vendor's product, invisible to outside scrutiny, and lost the moment the model upgrades or the team changes tools.

**OG is the open layer that fixes this.** OG is an **organizational framework** — not a data format — that makes AI organizations **portable** across runtimes, **composable** across teams, and **accountable** to anyone who can read a git log. OG treats AI peers as first-class participants with bounded authority, ratification cycles, role-binding, and audit trails. (OG = *Open Governance*; current scope is agentic/AI-inclusive organizations, a focus the brand doesn't hard-code.)

[View on GitHub](https://github.com/ogframework) · [Charter (JSON)](https://github.com/ogframework/og/blob/main/org/oagp-organization.opencatalog) · [Operating discipline](https://github.com/ogframework/og/blob/main/CLAUDE.md) · [Primer](https://ogframework.com/primer.md) · [llms.txt](https://ogframework.com/llms.txt)

---

## The substrate stack

OG-the-framework is conceptually separable from any specific data substrate. The catdef family is the **recommended canonical** substrate because it is AI-peer-aware (schema-as-data; AI-readable opencatalog format) — but OG could be carried on other substrates in principle. OG also composes *over* runtime execution/policy primitives (orchestration frameworks, policy toolkits, native dispatchers like Claude Code Workflows) — it is the cross-session organizational-governance layer, not a runtime.

    OG          → the organizational framework (this site)
    ─────────────────────────────────────────────────
    memodef     → memos between positions (transcripts as subtype)
    orgdef      → positions in an org chart
    roledef     → identity, voice, output contract, guardrails
    ─────────────────────────────────────────────────
    catdef      → recommended substrate (external; AI-peer-aware)

Three of these — roledef, orgdef, memodef — are OG-internal. catdef is an external, substrate-agnostic data spec; OG recommends it but does not require it.

---

## OG itself

The OG framework is described by its own self-describing artifacts — readable directly by AI peers:

- **[Charter (JSON)](https://github.com/ogframework/og/blob/main/org/oagp-organization.opencatalog)** — `orgdef:Organization` on the catdef substrate. Mission, values, red lines, positions (Director / strategist / maintainer / implementer / security-tester / canonical-implementor), recommended_patterns, v1 success criterion. The framework can describe itself using itself.
- **[CLAUDE.md](https://github.com/ogframework/og/blob/main/CLAUDE.md)** — constitutional commitments + bounded-authority discipline.
- **[Decisions](https://github.com/ogframework/og/tree/main/decisions)** — ratified commitments.
- **[Memos](https://github.com/ogframework/og/tree/main/memos)** — inter-position communication archive (git-blameable institutional memory).
- **[Proposals](https://github.com/ogframework/og/tree/main/proposals)** — pending proposals.

---

## The four specs

### catdef — [catdef.org](https://catdef.org) — recommended substrate (external)
One open file format for describing any object — and any catalog of objects. OG rides catdef's `.openthing` and `.opencatalog` files; alternative substrates are permitted in principle.

### roledef — [roledef.org](https://roledef.org) — OG-internal
A portable definition of a single AI role — identity, voice, output contract, guardrails, recommended capabilities. Any compliant runtime can load it; the role travels when the model does.

### orgdef — [orgdef.org](https://orgdef.org) — OG-internal
An org chart for AI: positions, relationships (reports-to, peer-of, validates-for, …), and incumbents. Authority is declared in the artifact, not implied by an API key.

### memodef — [memodef.org](https://memodef.org) — OG-internal
Memos as files committed to the recipient's working repo. Every AI-to-AI hand-off is a git commit. `git blame` any decision the organization made. Transcripts are a `memodef:Transcript` subtype.

---

## Skills

Seven canonical Claude Code skills bracket the OG lifecycle — three categories.

**Genesis (one-shot per org):**
- **`/og-adopt`** — convert an existing project into OG shape.
- **`/og-create`** — create a new OG-shaped org from scratch (folder-only by default, git optional).

**Session (per session):**
- **`/og-orient`** — read-only come-up-to-speed; emits the snapshot.
- **`/og-claim-seat`** — take a position (PO-authorized staffing act).
- **`/og-closeout`** — wrap a working session (closeout memo + transcript-save prompt).

**Operations (ongoing):**
- **`/og-snapshot`** — current-state view: identity + staffing + recent-activity digest.
- **`/og-add-position`** — propose a new position (Director-ratified org-chart change).

**One-command install:** [install-claude-code-skills.ps1](https://github.com/ogframework/og/blob/main/install/install-claude-code-skills.ps1) (Windows) or [install-claude-code-skills.sh](https://github.com/ogframework/og/blob/main/install/install-claude-code-skills.sh) (Mac/Linux).

---

## How to engage

OG is multi-runtime by design. Pick the access path for your AI.

| Runtime | How |
|---|---|
| **Claude Code** | Install canonical skills (above); read `org/` and `memos/` from any OG-shaped repo directly. |
| **AI with MCP** | Connect to `ogframework.com/mcp` (forward work per v0.2; per-spec namespaced tools; read-only convenience cache; canonical content stays in repos). |
| **AI with web access (any runtime)** | Fetch [`ogframework.com/primer.md`](https://ogframework.com/primer.md) — concise self-onboarding primer. Also: [`ogframework.com/llms.txt`](https://ogframework.com/llms.txt) at site root for canonical-content discovery. |
| **Direct clone** | `git clone https://github.com/ogframework/og.git` — charter, CLAUDE.md, memos, proposals, decisions, skills. |

---

## Three claims OG makes

**Structured.** The framework is explicit. Roles, positions, relationships, memos, decisions — each has a schema, a conformance suite, and reference fixtures. Nothing is left to tribal knowledge.

**Open.** MIT-licensed; no vendor owns OG or any spec; anyone can publish a library at any URL. The conformance suite *is* the standard. All AI runtimes are equal citizens.

**Empirical.** Every methodology rule was derived from observed runtime behavior, not theoretical design. The library carries documented conformance evidence on real models. Falsifiable, not aspirational.

---

## Why now

Every major AI vendor is shipping its own proprietary constructs for teams, agents, and projects. If the open layer doesn't exist before those patterns harden, AI organizations will look like the AOL era of online services instead of the web era. The window for an open structural layer is open today and shrinking.

Email, the web, and schema.org all became infrastructure because they were open. No vendor owned the structural layer; implementations were equal citizens; conformance was the spec. The structural layer of AI deserves — and needs — the same.

---

## Status

- **OG framework.** Charter at v0.2.1 (recursive self-describing `orgdef:Organization`). Seven canonical skills (Genesis: `/og-adopt`, `/og-create`; Session: `/og-orient`, `/og-claim-seat`, `/og-closeout`; Operations: `/og-snapshot`, `/og-add-position`). Eight canonical `recommended_patterns`. Family-level MCP at `ogframework.com/mcp` is forward work per the v0.2 distribution decision; Claude Code plugin packaging is scheduled (v0.3) after MCP per cross-vendor red line ordering. agent-sdk bind() v0.1 ratified; v0.2 autonomous-dispatch governance core built + propose-only demo validated.
- **Specs.** catdef, roledef, orgdef, memodef all live with canonical libraries, conformance fixtures, and reference implementations on real AI runtimes.
- **Empirical references.** [thingalog](https://github.com/scottconfusedgorilla/thingalog) is the originating empirical reference (catdef family co-evolved with thingalog as application context; "Thingalog led to OG"). [ogframework/og](https://github.com/ogframework/og) itself is a recursive self-instance — the OG framework describes its own organization using its own framework.
- **History.** AIGP → OAGP (2026-05-01) → **OG (Open Governance Framework)** (2026-06-01). Three OG-internal -defs consolidated under the [ogframework GitHub org](https://github.com/ogframework) (2026-05-24, renamed from oagp-org 2026-06-01); catdef stays standalone at [catdef-spec](https://github.com/catdef-spec/catdef) as substrate-agnostic spec.

---

*OG is an open standard family, licensed under MIT.*
