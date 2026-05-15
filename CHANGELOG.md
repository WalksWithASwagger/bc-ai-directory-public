# Changelog

## v1.5.0 — May 14, 2026

People enrichment pass: R–T range profiles (batch-08), quality correction for 8 incorrectly included stubs.

- **963 organizations** exported (unchanged)
- **833 people** exported (was 835; +6 new validated, -8 stubs correctly removed)
- Batch-08: Pradeepa Dhanasekar (Able, Burnaby), Stephen Makonin (SFU Adjunct Prof, Computational Sustainability Lab), Tito Ferradans (Vancouver filmmaker/AI tools), Tris Hussey (Chilliwack AI consultant, Peak Intelligence), Talesh Seeparsan (Bit79, OWASP LLM Security) promoted
- Quality fix: 8 stub profiles (U–V range) removed from export that were incorrectly included in v1.4.0 due to uncontrolled agent run

## v1.4.0 — May 14, 2026

People enrichment pass: J–K range profiles (batches 05–07), Web Summit day-3 recap.

- **963 organizations** exported (unchanged)
- **835 people** exported (was 822; +13 from batches 05–07 promotions)
- Batch-05: Jordan Kallman, Jordan Taylor, Jos Duncan Asé, Joseph Kibur, Joseph McCaig, Joseph Pallant, Josh Arlitt promoted
- Batch-06: Josh Loh, Joshua Gardner, Joshua Michie, Julia Morton, Julian Lee (×2), Juliana enriched
- Batch-07: Kris Krüg (BC + AI founder/ED), Kate Armstrong, Lawrence Okolo promoted; Kevin Friel profile rewritten
- Web Summit Vancouver 2026 Day 3 recap added to project docs

## v1.3.0 — May 14, 2026

People enrichment pass: public-source research on G–O range profiles, privacy cleanup, batch-04 promotions.

- **963 organizations** exported (unchanged)
- **822 people** exported (was 695; +127 from L–O shard enrichment — founders, researchers, operators promoted after public-source verification)
- People enrichment batch-04: 4 new promoted profiles (Gabriel Zaro, Jacob DePodesta, James Hursthouse, Jessica Liang)
- L–M–N–O shard: 271 profiles enriched with public sources; roles, organizations, and summaries updated
- Privacy sweep: email addresses and phone numbers removed from public-facing profile bodies across multiple profiles

## v1.2.0 — May 14, 2026

Data enrichment pass: category normalization, website backfill, location inference, people-org linking.

- **963 organizations** exported (unchanged)
- **695 people** exported (was 566; additional active community members included)
- Categories collapsed from 560 unique values → 27 canonical categories (AI/ML, Health Tech, Climate Tech, Enterprise SaaS, Creative Tech, Robotics & Automation, etc.)
- 134 organization website URLs backfilled from validation source notes
- 79 organization locations inferred from profile summary text
- 146 people profiles linked to their affiliated organizations
- Category normalization applied across 919 org profiles

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
