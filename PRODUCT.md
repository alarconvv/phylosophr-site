# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

static HTML/CSS (user's explicit choice; no framework, no build step)

## Users

Two audiences, both from the evolutionary/phylogenetic comparative biology (PCM) research community:

1. **Researchers evaluating phyloSophR** — biologists who work with phylogenetic comparative methods and are sizing up whether this tool (still in dissertation-proposal stage) would help their own research workflow and reproducibility practices.
2. **Potential annotation contributors** — researchers who might annotate their own publications, and student volunteers, who are deciding whether to get involved in the community-annotation effort that will build phyloSophR's training corpus. This second audience is the primary reason this site exists.

## Product Purpose

Present phyloSophR — an open research project for reproducible phylogenetic comparative biology, developed as part of a PhD at UMB — to its research community: what it is, why it matters, and — centrally — the community-annotation initiative that will grow its training corpus. Success is a visitor who (a) understands the reproducibility problem phyloSophR addresses and how it addresses it, and (b) understands the community-annotation idea clearly enough to want to get involved later.

**Framing note (updated 2026-09-22 at the user's explicit direction):** the site presents phyloSophR as a project to its community, not as an explainer of an academic proposal document. Drop meta-references to "the proposal" ("the proposal says...", "from the proposal," "the proposal names...") in favor of direct project voice ("phyloSophR does...", "phyloSophR plans to..."). The underlying honesty constraints below are unchanged by this reframing — only the narrating voice changes, not the facts or their hedging.

This is a companion **explainer/landing site**, separate from the existing interactive Shiny prototype in the sibling `phylosophr-demo/` project (which lets someone click through the hypothesis→DAG→preregistration workflow). This site explains *why* and *what*; the demo shows *how*. Do not duplicate the demo's UI here.

## Positioning

phyloSophR is not just a workflow-assistant tool — it is one whose own training data is built the same way it asks researchers to work: openly, transparently, and collaboratively. Where existing PCM tools are closed, single-author-maintained R packages with English-only documentation, phyloSophR (1) turns a natural-language hypothesis into a pre-registerable, auditable DAG before any data collection, explicitly to prevent p-hacking/HARKing, and (2) builds its own underlying domain-language corpus through open, credited community annotation rather than proprietary labeling — positioning annotation itself as "work done by the community, for the community."

## Operating Context

- phyloSophR is an **early-stage academic research project**, not a funded, running, or fully shipped initiative — developed as part of a PhD at UMB, advised by Dr. Liam J. Revell. Present it in first-person project voice, not as a summary of a proposal document.
- The community-annotation task is **planned, not active**: an initial team of 3 annotators will double-annotate a training corpus first; opening annotation to the wider community (researchers annotating their own publications, student volunteers) is the next planned phase.
- Potential supporting organizations — Open Science Framework, AI for Science, the Turing Institute, rOpenSci — are **potential/aspirational partners phyloSophR hopes will support the initiative**, not confirmed collaborators or sponsors. Do not present them as committed partners or use their names/logos as endorsements.
- Precedent: the Smithsonian Institution's Neotropical Studies model of volunteer-driven documentation and museum-label annotation, which inspired the "community certificates / acknowledgment in dataset documentation" incentive idea.
- The sibling interactive Shiny prototype (`../phylosophr-demo/`) is now **live at `https://alarconvv.shinyapps.io/phylosophr-demo/`**, and is linked from this site's header as "Live Demo." (Superseded 2026-09-22: earlier text here said no public URL existed — that's no longer true.)

## Capabilities and Constraints

- **No real sign-up, contact form, or intake mechanism exists yet.** Per the user's explicit decision, this site is informational only for now. Any call-to-action must be honest about that — e.g., a plain `mailto:` contact rather than a fabricated signup form, waitlist, newsletter, or "join now" flow with no backend.
- **No real annotation tool exists yet either.** Do not depict, mock up, or imply a working annotation interface; the annotation methodology (double annotation, Prodigy, active learning, inter-annotator agreement via Cohen's Kappa/Krippendorff's Alpha) is real content from the proposal but is describing a *planned* process, not a live product.
- **No testimonials, user counts, case studies, or press exist.** None may be fabricated or implied (no "join 200 researchers," no logos-of-partners bar, no quotes).
- Contact: `vivianaromeroalarcon@umb.edu` (confirmed 2026-09-22) is the real contact address, used in the "Get in touch" mailto link.
- Source content for this site's copy must stay factually traceable to the underlying dissertation proposal (`Proposal/writing/Draft_VivianaRomeroAlarcon_UMB_Proposal_V260511_ref.pdf`, PDF pages 6–14 / printed pages 5–13, sections 3.1–3.1.6) — real methodology, real numbers, real examples — even though the page voice no longer refers to "the proposal" as a document. Do not invent claims the source material doesn't support.

## Brand Commitments

- Name: **phyloSophR** (a portmanteau of "phylo" and "Sophos," meaning wiser).
- A hex-sticker logo asset already exists (owl on a branch inside a navy hexagon, teal/navy coloring) and is in use at `../phylosophr-demo/www/logo.png`. Reuse this exact asset rather than generating a new mark.
- The sibling interactive demo already established a deliberate visual identity — Flatly-derived navy (`#2C3E50`)/turquoise (`#18BC9C`)/amber (`#F39C12`) palette, IBM Plex Sans/Mono typography, flat shapes (4–8px radii, hairline borders, no soft shadows) — arrived at over several rounds of explicit user direction ("scientific plain style," "follow the Shiny theme Flatly"). This is strong evidence for the visual world this site should share, so the two phyloSophR surfaces read as one project — but the exact treatment (this is a Persuade-mode landing page, not an Operate-mode tool UI, so it can be bolder/more editorial) is a new-work decision, not locked here.
- **Standing direction preference (confirmed 2026-09-22):** offered a bolder, product-authentic herbarium/specimen-label visual world (concept-seed key `9bdf7e4b`, assigned index 3) for this surface; the user took the standing exit and chose the plain/conventional academic-tool register instead, referenced against R-package/pkgdown documentation sites (tidyverse.org, ropensci.org) and a university lab/research-group site. This canon choice carries the existing navy/turquoise/amber + IBM Plex system as-is, with no additional visual material layered in. Treat "plain, content-first, pkgdown-register" as the standing default for future surfaces on this site unless the user says otherwise.

## Evidence on Hand

- The dissertation proposal PDF is the sole source of real project content. No other written materials, data, or assets exist for this site beyond the logo.
- State explicitly for future work: there are no user quotes, no screenshots of a working annotation tool, no partner-organization confirmations, and no deployed demo URL to link to. Do not invent any of these.

## Product Principles

1. **Never overstate project status.** This is a dissertation proposal in progress; every claim about capability, partnership, or availability must read as planned/aspirational where the source material says so, not as shipped or confirmed.
2. **The community-annotation idea is the centerpiece**, not a footnote — it's the specific reason this site was requested. Explain the mechanism (why annotation is hard, why it takes multiple annotators, how the community model helps) as clearly as the tool itself.
3. **No fabricated participation mechanics.** No signup forms, waitlists, member counts, or partner logos that don't exist. A plain, honest "here's the idea; reach out if interested" is correct; a fake CTA flow is not.
4. **Speak to both audiences without splitting the page into two disconnected halves** — a researcher deciding whether phyloSophR is useful and a potential annotator deciding whether to get involved are reading the same reproducibility argument from different angles.
5. **Complement, don't duplicate, the interactive demo.** This site is the "why/what"; it can mention the prototype exists without trying to be it.

## Accessibility & Inclusion

No specific standard was mandated in this session. Given the academic/community audience and the companion demo's existing WCAG 2.1 AA work, build this site to the same bar by default (semantic HTML, sufficient color contrast, keyboard-navigable, meaningful alt text) unless the user says otherwise.
