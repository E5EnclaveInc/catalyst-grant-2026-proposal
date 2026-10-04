# Provenance-Native Evidence Synthesis Agent — Proposal, Digital Science Catalyst Grant 2026

## 1. THE PROBLEM
Whose problem is this, and what do they do about it today?

Human-rights and community researchers run on evidence that has to hold up under scrutiny — courtrooms, funder audits, peer review. Today that evidence is synthesized by hand: researchers read hundreds of primary sources, keep notes in documents and spreadsheets, and assemble narratives whose provenance lives in memory, not in the record. When a claim is challenged, the trail is reconstructed backward — slowly, and sometimes not at all.

AI made the synthesis fast and the provenance problem worse. A generic chatbot summarizes fifty sources in minutes — but with invented citations, silently reordered facts, and no record of which source supported which sentence. For research whose credibility is its currency, this is unusable.

The researchers who most need agentic help with evidence — advocates, journalists, community scholars documenting injustice — cannot touch these tools, because no existing agent *shows its working*.

## 2. YOUR WORKFLOW
Walk us through what your agent does, step by step, from trigger to output. Which steps run autonomously, and where does a person review, approve or override? Which existing tool or system does it run inside, and who uses that tool today?

We are building a provenance-aware evidence-synthesis agent inside the researcher's documentation workflow:

1. **Ingest.** The researcher loads primary sources — transcripts, court filings, public records, reports, datasets — into a case workspace. Each source is registered with origin metadata before the agent reads it.
2. **Draft with receipts.** The researcher asks a question (e.g., "What do the sources say about housing-code enforcement on this block, 2019–2024?"). The agent searches the corpus, extracts passages, drafts an answer, attaching **every sentence to its supporting passages** — inline machine-checkable citations, not decorative footnotes.
3. **Challenge pass.** Before finalizing, the agent runs a mandatory self-audit: it re-verifies each cited claim, flags thin support or contradictions, and quarantines anything ungrounded as **unsupported — excluded from the output, listed separately.**
4. **Human review gate.** A reviewer sees the draft alongside the evidence map — each claim, its sources, its confidence flag — and approves or rejects claim-by-claim. Every decision is logged with approver and timestamp.
5. **Export the audit bundle.** The final document ships with the full trail: source registry, claim-to-passage map, challenge-pass log, review decisions. A skeptical reader traces any sentence to its source unaided.

Its first users are the advocacy organizations, community researchers, and journalists the applicant already works with.

## 3. TRUST, AUDIT AND GOVERNANCE
How does a user see what the agent did, and why? How do you establish provenance for the sources and the outputs? What happens when the agent is uncertain or wrong, and who is accountable?

The agent acts autonomously *within* a governed pipeline — it can never silently assert. Trust is the architecture, not a feature:

- **Provenance-first data model.** Every source is fingerprinted at ingest. Claims point to passages, not documents. Altering a source visibly invalidates the claims that depended on it.
- **Mandatory self-audit.** The challenge pass cannot be skipped by prompt. Claims that fail verification are quarantined into an "unsupported" list — the agent never smooths over a gap.
- **Human-in-the-loop by design.** No output is final until a named human approves it claim-by-claim, with approver, timestamp, and decision recorded per claim.
- **No invented citations, structurally.** A citation to a source outside the registered corpus cannot be emitted — the current generation's failure mode is architecturally closed.

## 4. TEAM
The founders, their backgrounds, key people and any advisors. Why you picked this problem, and what domain expertise you bring.

The team is the founder-led core of E5 Enclave Inc. (Miami 501(c)(3) public charity), the applicant. The founder authored the 101-page empirical record *The Measure of the Wound* on systemic harm in Black Miami, published with a Zenodo DOI (10.5281/zenodo.22676045), plus the underlying Black Distress Index dataset — assembled by hand from scattered primary sources, under challenge. The concept grows out of that documentation work: the provenance pain is lived, not theorized.

The founder's organization already operates production multi-step AI agent systems — autonomous agents that reconnoiter, vet, draft, stage, and submit under human gating, with audit trails on every action. The team builds agentic workflows it depends on daily, for the hardest kind of user: a researcher whose every claim must survive challenge.

## 5. WHERE YOU ARE TODAY
Current stage: concept, prototype, working product, or in use with real users. What exists now. Any users or customers, and what you have done to test the idea.

Well-formed concept moving to prototype. What exists: the governed-pipeline design and a genuine published test corpus — *The Measure of the Wound* (Zenodo DOI 10.5281/zenodo.22676045) plus the Black Distress Index dataset. No prototype, codebase, or demo yet. The grant builds the first working prototype — tested against our own corpus, with structured pilots run with real researchers. No users or customers yet.

## 6. ALTERNATIVES AND COMPETITORS
How is this solved today, including by doing nothing? Who else is working on it, and at what size and stage? How are you different?

Solved by hand: researchers read hundreds of sources and assemble narratives whose provenance lives in memory, documents, and spreadsheets. By generic AI chatbots: fast synthesis with invented citations and no audit trail — unusable for evidence that must survive challenge. By doing nothing: high-stakes research communities largely avoid agentic AI for synthesis, because nothing they can touch *shows its working*.

Research-integrity tools and LLM vendors are adding citation features. We differ architecturally: not a chatbot with footnotes. The challenge pass cannot be bypassed by prompt; citations resolve only against the registered corpus; every claim carries its approver, timestamp, and decision; the audit bundle is readable without our software.

## 7. WHERE THIS GOES
Your longer-term vision for the product. If it is a commercial product, who would pay and what is your pricing thinking?

The prototype proves the model on one corpus (our own). The path after:

1. **Researcher pilots.** Advocacy organizations, community researchers, and journalists working on documented cases use the tool on live work; their feedback hardens the review interface and validates the audit bundle against real scrutiny.
2. **Corpus connectors.** Ingest adapters for the repositories researchers already use (open-access platforms, public-records systems, data archives), so the tool meets researchers where their sources live — including workflows that already touch Digital Science infrastructure.
3. **The standard, not just the tool.** The audit-bundle format is readable without our software. If it is adopted as a norm for defensible AI-assisted evidence work, the tool's value compounds: any reviewer can verify any bundle.

We go to market through the researchers whose credibility depends on it: first the advocacy and community-research world, then the institutions that train and fund them. No pricing page yet — this is the workflow layer that lets agentic AI touch high-stakes research at all.

## 8. FIT WITH DIGITAL SCIENCE
Which part of the research lifecycle do you sit in, and which audience: researchers, institutions, publishers, funders or industry. Why would you want to work with us on this problem?

We sit in **evidence synthesis** and **research integrity** — where a researcher's sources become claims, and where current AI tooling fails the audit test. Our audience is researchers first (advocacy researchers, community scholars, journalists, and the institutions that employ and fund them) — people whose output must survive challenge in courtrooms, newsrooms, and peer review.

This complements — not duplicates — Digital Science's portfolio: Dimensions maps what research exists, Altmetric maps its attention, Figshare preserves its outputs. None governs the *synthesis step* where an agent turns sources into claims — the gap a provenance-native evidence agent fills, for the researchers their products already serve.

## 9. BUDGET
How you would spend up to £25,000, and what it would let you do that you cannot today.

Up to £25,000 funds the first prototype: contract engineering for the ingest/registry layer, claim-to-passage citation engine, mandatory challenge pass, and claim-by-claim review interface (the largest share); model API and hosting costs for the prototype against our published corpus; provenance data-model and exportable audit-bundle work; structured pilots with real researchers, compensating their time.
