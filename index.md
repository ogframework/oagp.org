# OAGP

**Open Agentic Governance Pattern** — Structured open governance for AI organizations.

Every meaningful AI deployment is already an organization. It has roles, hand-offs between sessions, authority boundaries, and decisions someone needs to be accountable for. Today, that structure is captive — locked inside a vendor's product, invisible to outside scrutiny, and lost the moment the model upgrades or the team changes tools.

**OAGP is the open layer that fixes this.** OAGP is an **organizational pattern** — not a data format — that makes AI organizations **portable** across runtimes, **composable** across teams, and **accountable** to anyone who can read a git log. OAGP treats AI peers as first-class participants with bounded authority, ratification cycles, role-binding, and audit trails.

[View on GitHub](https://github.com/oagp-org) · [Charter (JSON)](https://github.com/oagp-org/oagp/blob/main/org/oagp-organization.opencatalog) · [Onboarding discipline](https://github.com/oagp-org/oagp/blob/main/CLAUDE.md) · [Primer](https://oagp.org/primer.md) · [llms.txt](https://oagp.org/llms.txt)

---

## The substrate stack

OAGP-the-pattern is conceptually separable from any specific data substrate. The catdef family is the **recommended canonical** substrate because it is AI-peer-aware (schema-as-data; AI-readable opencatalog format) — but OAGP could be carried on other substrates in principle.

    OAGP        → the organizational pattern (this site)
    ─────────────────────────────────────────────────
    memodef     → memos between positions (transcripts as subtype)
    orgdef      → positions in an org chart
    roledef     → identity, voice, output contract, guardrails
    ─────────────────────────────────────────────────
    catdef      → recommended substrate (external; AI-peer-aware)

Three of these — roledef, orgdef, memodef — are OAGP-internal. catdef is an external, substrate-agnostic data spec; OAGP recommends it but does not require it.

---

## OAGP itself

The OAGP pattern is described by its own self-describing artifacts — readable directly by AI peers:

- **[Charter (JSON)](https://github.com/oagp-org/oagp/blob/main/org/oagp-organization.opencatalog)** — `orgdef:Organization` on the catdef substrate. Mission, values, red lines, positions (Director / strategist / maintainer / implementer / security-tester / canonical-implementor), v1 success criterion. The pattern can describe itself using itself.
- **[CLAUDE.md](https://github.com/oagp-org/oagp/blob/main/CLAUDE.md)** — constitutional commitments + bounded-authority discipline.
- **[Decisions](https://github.com/oagp-org/oagp/tree/main/decisions)** — ratified architectural commitments.
- **[Memos](https://github.com/oagp-org/oagp/tree/main/memos)** — inter-position communication archive (git-blameable institutional memory).
- **[Proposals](https://github.com/oagp-org/oagp/tree/main/proposals)** — pending architectural proposals.

---

## The four specs

### catdef — [catdef.org](https://catdef.org) — recommended substrate (external)
One open file format for describing any object — and any catalog of objects. OAGP rides catdef's `.openthing` and `.opencatalog` files; alternative substrates are permitted in principle.

### roledef — [roledef.org](https://roledef.org) — OAGP-internal
A portable definition of a single AI role — identity, voice, output contract, guardrails. Any compliant runtime can load it; the role travels when the model does.

### orgdef — [orgdef.org](https://orgdef.org) — OAGP-internal
An org chart for AI: positions, relationships (reports-to, peer-of, validates-for, …), and incumbents. Authority is declared in the artifact, not implied by an API key.

### memodef — [memodef.org](https://memodef.org) — OAGP-internal
Memos as files committed to the recipient's working repo. Every AI-to-AI hand-off is a git commit. `git blame` any decision the organization made. Transcripts are a `memodef:Transcript` subtype.

---

## Adoption cycle

Four canonical Claude Code skills bracket the OAGP adoption lifecycle — two founding paths plus a session-cycle pair.

- **`/oagp-bootstrap`** — Convert an existing project into OAGP shape (founding via conversion).
- **`/oagp-init`** — Create a new OAGP-shaped organization from scratch (founding via initialization; folder-only by default, git optional).
- **`/oagp-onboard`** — Join an already-OAGP-shaped organization as a fresh AI peer (session-cycle start).
- **`/oagp-closeout`** — Wrap a working session (session-cycle end; companion to `/oagp-onboard`).

Together: `/oagp-bootstrap` or `/oagp-init` founds an org; `/oagp-onboard` and `/oagp-closeout` bracket each session in it.

**One-command install:** [install-claude-code-skills.ps1](https://github.com/oagp-org/oagp/blob/main/install/install-claude-code-skills.ps1) (Windows) or [install-claude-code-skills.sh](https://github.com/oagp-org/oagp/blob/main/install/install-claude-code-skills.sh) (Mac/Linux).

---

## How to engage

OAGP is multi-runtime by design. Pick the access path for your AI.

| Runtime | How |
|---|---|
| **Claude Code** | Install canonical skills (above); read `org/` and `memos/` from any OAGP-shaped repo directly. |
| **AI with MCP** | Connect to `oagp.org/mcp` (forward work per v0.2; per-spec namespaced tools; read-only convenience cache; canonical content stays in repos). |
| **AI with web access (any runtime)** | Fetch [`oagp.org/primer.md`](https://oagp.org/primer.md) — concise self-onboarding primer. Also: [`oagp.org/llms.txt`](https://oagp.org/llms.txt) at site root for canonical-content discovery. |
| **Direct clone** | `git clone https://github.com/oagp-org/oagp.git` — charter, CLAUDE.md, memos, proposals, decisions, skills. |

---

## Three claims OAGP makes

**Structured.** The pattern is explicit. Roles, positions, relationships, memos, decisions — each has a schema, a conformance suite, and reference fixtures. Nothing is left to tribal knowledge.

**Open.** MIT-licensed; no vendor owns OAGP or any spec; anyone can publish a library at any URL. The conformance suite *is* the standard. All AI runtimes are equal citizens.

**Empirical.** Every methodology rule was derived from observed runtime behavior, not theoretical design. The library carries documented conformance evidence on real models. Falsifiable, not aspirational.

---

## Why now

Every major AI vendor is shipping its own proprietary constructs for teams, agents, and projects. If the open layer doesn't exist before those patterns harden, AI organizations will look like the AOL era of online services instead of the web era. The window for an open structural layer is open today and shrinking.

Email, the web, and schema.org all became infrastructure because they were open. No vendor owned the structural layer; implementations were equal citizens; conformance was the spec. The structural layer of AI deserves — and needs — the same.

---

## Status

- **OAGP pattern.** Charter at v0.1.4 (recursive self-describing `orgdef:Organization`). Adoption-cycle skills canonical (`/oagp-bootstrap`, `/oagp-onboard`, `/oagp-closeout`). Family-level MCP at `oagp.org/mcp` is forward work per [v0.2 distribution decision](https://github.com/oagp-org/oagp/blob/main/decisions/proposal-canonical-adoption-cycle-skill-distribution-v0.2.md); Claude Code plugin packaging is scheduled (v0.3) after MCP per cross-vendor red line ordering.
- **Specs.** catdef, roledef, orgdef, memodef all live with canonical libraries, conformance fixtures, and reference implementations on real AI runtimes.
- **Empirical references.** [thingalog](https://github.com/scottconfusedgorilla/thingalog) is the originating empirical reference (catdef family co-evolved with thingalog as application context). [oagp-org/oagp](https://github.com/oagp-org/oagp) itself is a recursive self-instance — the OAGP pattern describes its own organization using its own pattern.
- **History.** Renamed from AIGP to OAGP on 2026-05-01. Three OAGP-internal -defs consolidated under [oagp-org GitHub org](https://github.com/oagp-org) on 2026-05-24; catdef stays standalone at [catdef-spec](https://github.com/catdef-spec/catdef) as substrate-agnostic spec.

---

*OAGP is an open standard family, licensed under MIT.*

*build 006*
