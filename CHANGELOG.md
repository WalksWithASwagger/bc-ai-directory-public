# Changelog

## v1.1.0 — May 14, 2026

Quality audit pass: automated false-positive sweep removed 67 incorrect "validated" profiles.

- **963 organizations** exported (was 1026; 67 removed — government agencies not meeting AI company criteria, non-BC HQs, defunct/rebranded entities, unverifiable companies)
- **566 people** exported (was 569; minor adjustment)
- Automated phrase-scanning now catches profiles where validation agents set `status: validated` while documenting contradictory findings
- Added CONTRIBUTING.md and GitHub issue templates to repository
- Added portal methodology/about page at `/bc-ai-directory/about`
- Added case statement document (BC-AI-DIRECTORY-CASE-STATEMENT.md)
- All 91 unit tests passing; export integrity verified (0 duplicates, 0 missing required fields)

## v1.0.2 — May 13, 2026

Validation swarm pass: 8 parallel agent batches processed 192 candidates from the remaining queue.

- **1026 organizations** exported (was 845; +181 newly validated)
- **569 people** exported (was 544; +25 additional profiles completed)
- Validated organizations across AI consulting, university research labs, government digital services, agritech, health tech, robotics, and SaaS
- Rejected candidates for: non-BC HQ, no AI relevance, defunct operations, unverifiable BC presence

## v1.0.1 — May 13, 2026

Quality audit pass: removed 21 false-positive "validated" profiles.

- **845 organizations** exported (was 865; 21 removed)
- **544 people** exported (was 524; 20 additional profiles completed)
- Removed profiles where agent validation runs had set `status: validated` but summaries documented finding no BC presence, no AI relevance, or no company at that name

## v1.0.0 — May 13, 2026

Initial public release.

- **865 organizations** validated and exported
- **524 people** validated and exported
- Schema: `bc-ai-directory-public-v1`
- Formats: JSON, CSV (organizations, people)
- License: CC BY 4.0
- Validation methodology documented in METHODOLOGY.md

### Coverage
- Geographic: British Columbia, Canada — primarily Vancouver, Victoria, Kelowna; smaller communities included
- Categories: AI/ML development, health tech, climate tech, agritech, creative tech, government/policy, research and academia, Indigenous technology, robotics, fintech
- Sources: BCTech, Crunchbase, PitchBook, LinkedIn, Luma event data, partner referrals, public sector funding announcements

### Quality notes
- Rejected 396 organizations from initial candidate pool for geographic misclassification, defunct status, or no AI relevance
- 884 additional candidates remain in `needs_external_public_sources` state — not yet validated, not included
- One false-positive (Vista Centre) caught and removed in pre-launch quality audit
