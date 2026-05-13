# Changelog

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
