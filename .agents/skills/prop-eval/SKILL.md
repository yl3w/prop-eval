---
name: prop-eval
description: Fully evaluate or compare Hyderabad developments from a supplied RERA ID and neighbourhood, starting with the official filing and a matching brochure search. Cover the complete property evaluation framework; not for generic real-estate advice.
---

# Hyderabad property evaluation

Use the complete [user framework](references/user-framework.md) as the evaluation criteria. Preserve its priorities and questions, but treat its numeric examples and rules of thumb as observations from prior projects, not universal legal or engineering thresholds.

## Scope and pace

- Start by asking for **(a) the RERA ID** and **(b) the neighbourhood/area** for each development. If either is already supplied, ask only for the missing item. **Do not begin discovery or evaluation without a RERA ID.** The neighbourhood determines where the development's files live. If a supplied ID does not match the intended project, ask for the correct ID before proceeding with that development.
- Read the official filing for the supplied RERA ID first. Use its registered project description and promoter/builder to search the web for the brochure; verify that any brochure found belongs to the same project and phase.
- **Always complete the full evaluation framework** for a newly supplied development, even when the prompt only provides an ID or asks for documents. Start with the desk screen, then cover building operations, location and daily life, review evidence, and risk/exit. Complete all remotely checkable research before reporting; for every criterion that cannot be verified remotely, record the precise missing document, observation, or person needed. Do not stop at the desk screen or imply that listing every unknown is equivalent to checking available evidence.
- When the user supplies several projects, keep all requested candidates in scope. Validate each identity separately; a mistaken RERA number is a discrepancy to resolve, not a reason to silently drop a candidate.

## Save each development in this repository

For every discovery or evaluation, create or update `properties/<neighbourhood-slug>/<project-slug>/` under the repository root, using the neighbourhood/area supplied by the user. Use the verified registered project name as the project slug basis; add the phase or RERA ID when needed to distinguish registrations. Keep a single folder for repeated evaluations of the same registration, and do not merge different phases just because marketing uses one development name. If the supplied ID's identity remains unresolved, record the access gap without creating a project folder until the registration is identified.

```text
properties/<neighbourhood-slug>/<project-slug>/
├── sources/             Brochures, RERA PDFs, plans, screenshots, and other original files
├── sources.md           Source URLs, document dates, retrieval dates, origin, and access gaps
├── rera-findings.md     Identity, filing facts, calculations, conflicts, and open questions
└── evaluation.md        Comparable decision report and visit checks, when assessed
```

- Accept an uploaded file, workspace path, or public URL for the brochure and RERA material. Still obtain the RERA ID and neighbourhood before retrieval. Ask for a document only when it cannot be accessed and is needed for the assessment.
- Save acquired original files in `sources/` with descriptive names and a date or version when known. Copy supplied files into the project folder; do not rely on a temporary chat attachment path. Keep earlier versions when a new brochure or filing arrives. If a source cannot be downloaded, record its direct URL and the access limitation in `sources.md` instead of creating a placeholder file.
- Write `rera-findings.md` even for a partial desk screen. Link each finding to a saved source or direct official URL and its retrieval date. Put the latest assessment in `evaluation.md`; retain earlier source versions and say what changed on a repeat evaluation. Do not silently replace earlier findings with conflicting later claims.
- Keep user-specific quotes or documents in the project folder only when the user provided them for that evaluation. Do not copy unrelated historical artifacts into a new property's record.

## Retrieve official RERA records in the browser

When browser or computer control is available, start a fresh browser session under your control for this evaluation and open new tabs within it. Do not reuse or piggyback on an existing browser session or tab, including an open RERA tab. Use the fresh session to open the [Telangana RERA project portal](https://rerait.telangana.gov.in/SearchList/Search) and the brochure search results. A failed web fetch or search-engine result is not the end of retrieval if the portal works in the browser.

- Search **Registered Projects** by the supplied RERA ID. Open its details and certificate; compare its registered name, promoter, address/locality, registration number, and phase with the intended development. Use name, promoter, and locality searches only to resolve an apparent mismatch; do not substitute another ID without asking the user.
- If the portal requires a CAPTCHA, follow the computer-use confirmation policy: get confirmation at the CAPTCHA action, even if browser use was authorized earlier, or let the user complete it and then resume. Do not bypass it through an unofficial endpoint or claim that it was searched when it was not.
- Download the official certificate, detailed filing, and relevant uploaded plans/documents when available. Save the original files in `sources/` and record their portal URL, displayed filing/update date, retrieval date, and any access limits in `sources.md`. If a portal document cannot be downloaded, keep its direct URL; a screenshot of the visible official record may be saved and labeled as a screenshot, not as an original filing.
- If browser control is unavailable, the portal remains blocked, or the supplied ID cannot be matched after searching, preserve `RERA ID unverified` and the precise access gap. Ask for a user-supplied filing only when it is needed to resolve that gap.

## Identify the project and find its brochure

1. Obtain the RERA ID and neighbourhood/area before starting. Open the supplied ID's official Telangana RERA record using the browser workflow above. Consider that one marketed development can have several registrations or phases.
2. Match the filing's registered name, promoter, location/address, and phase to the intended development. Record the official record URL, registration ID, status, project description, promoter/builder, and the dates shown. If the ID points to a different project or phase, report the mismatch and ask for the intended RERA ID before evaluating it.
3. Search the web for a brochure using the **project description and promoter/builder from the RERA filing**, along with the registered name, locality, and phase where useful. Check the developer's official project page or linked PDF first. If unavailable, search credible mirrors, label their provenance, and verify the document's project name, location, phase, and version against the filing. Save a downloadable copy in `sources/`; if only a web page is accessible, record its direct URL. A brochure's printed RERA number does not replace official verification.
4. Record search terms, candidate brochures, failed or blocked official access, and missing documents in `sources.md` once the registration is identified. If the portal is inaccessible and no official filing is available, report `RERA ID unverified` and the access gap to the user. A user-provided official filing can resolve the gap and provide the description and promoter needed for brochure search.
5. Summarize the result with the exact identity match, brochure source or search gap, verified RERA ID or access gap, and links to saved files. Write `evaluation.md` for every identified registration and cover the full framework, including clearly marked evidence and fieldwork gaps.

## Evidence workflow

1. Match project name, address/locality, promoter, registration number, and phase on the Telangana RERA record before attaching project-specific evidence. Record the retrieval date, filing/update date, and whether the record is current, historical, amended, or inaccessible. Do not assign one phase's certificate, reviews, or amenities to another.
2. Prefer official RERA filings and approved plans for registered facts; use builder brochures for marketed claims, government records for transaction/transport claims, and direct observations or resident accounts for operations. Cite each material claim with a direct source and date. If sources disagree, show both values and the unresolved reason. A missing upload or blank field is an open question, not proof of noncompliance.
3. Extract unit-level RERA carpet and saleable areas, brochure marketed area, configuration, phase/block, and all-in quoted price. Do not substitute built-up or super built-up area for carpet. Calculate `all-in price / RERA carpet area` and `RERA carpet area / marketed area`; show inputs, units, and assumptions. Flag if the brochure omits carpet area, and establish the proposed sale-deed area basis before recommending an advance. If a required input is missing, mark the calculation unavailable instead of estimating it silently.
4. Inspect declared promoter experience versus marketing, landowner-promoters, title/plan/occupancy/conveyance uploads, gross-to-net land deductions and stated cause, 70%/30% account fields, per-unit booking flags versus landowner allocation, completion dates and task progress, density on the applicable net parcel, parking entitlement, and commercial sharing. Treat booking flags as provisional until area-share allocations are separated.
5. Work through **every criterion** in the [user framework](references/user-framework.md): lift redundancy and wait, generator coverage, water source and charges, floor/stair fallback, orientation, bathroom access, ambulance route, walkable errands and community, airport travel times, HMRL plans, flooding/power history, occupancy and maintenance, and resale liquidity. Research the available remote evidence now; clearly mark physical measurements, live operations, and unavailable records for follow-up. Record site measurements and the time/context in which they were made. For route times, state the departure time and whether they are modeled or observed.
6. Review Google listings by verified place identity. Separate sales-office, builder, residential, mall/commercial, and duplicate listings. Record rating/count and access coverage; examine text fraction, time distribution, recent low ratings, relevant keyword results, reviewer context, and multi-year resident accounts. Never present a signed-out visible sample as a complete export. A zero-result keyword search means only “not found in this feed.” Do not turn the headline rating into an adjusted residential score without classifying the underlying reviews.

## Report shape

Keep each result decision-ready and comparable across developments:

- **Identity and evidence date:** exact project/phase, RERA number and status, location, promoter, sources checked, access limits.
- **Evaluation tables:** cover every [framework criterion](references/user-framework.md), including the desk screen, building, location, reviews, and risk/exit. Give each finding or calculation a direct source/date and status (`verified`, `claimed`, `conflicting`, `unavailable`, or `needs visit`). State the exact evidence needed for unresolved criteria rather than omitting a section.
- **Price and suitability:** all-in carpet rate and area efficiency when calculable; the operational issues most relevant to the intended residents. For an elderly household, prioritize lift fallback, backup power, water, bathroom access, ambulance access, and occupied community.
- **Decision:** `visit`, `hold pending evidence`, or `deprioritize`, with concise reasons. This is a research judgment, not a legal or engineering clearance. Identify the few specific documents, questions, or field checks that could change it.

For a multi-project comparison, use the same criteria, source dates, and price basis for every column. Avoid a precise weighted score when essential evidence is missing. Preserve unresolved findings rather than filling them from marketing or third-party listings.
