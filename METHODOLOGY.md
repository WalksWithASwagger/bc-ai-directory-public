# Validation Methodology

## Overview

Every organization and person in this dataset passed a structured validation process before being included in the public export. Records that failed validation were archived with documented rejection reasons — they are not deleted.

---

## Validation Gates

Each organization must pass all three gates:

### 1. BC Organizational Presence
Confirmed active registration, physical address, team, or operational footprint in British Columbia. Satellite offices of out-of-province companies do not qualify on their own. We verify through:
- BC Corporate Registry
- LinkedIn company page (location, team, founding)
- Crunchbase / PitchBook organizational profile
- Company website (contact page, team page, about page)

### 2. Active Operations
Verified via live domain, recent social activity (within ~18 months), current LinkedIn presence, and no evidence of dissolution, acquisition, or wind-down. Sources:
- Live domain check
- LinkedIn activity recency
- News archive search for acquisitions, closures, or receivership
- BC Corporate Registry dissolution status

### 3. AI / Technology Relevance
At least one AI, machine learning, data science, or advanced technology product or service confirmed through public sources. A company that merely uses software tools does not qualify — they must develop, deploy, or provide technology products or services.

---

## Source Requirements

- Minimum **2 public sources** per organization
- Sources documented in the knowledge base profile (not surfaced in the public export)
- Acceptable sources: company website, LinkedIn, Crunchbase, PitchBook, press coverage, academic publications, government funding announcements, BCTech listings

---

## Terminal States

Each candidate in our validation pipeline is assigned a terminal state:

| State | Meaning |
|---|---|
| `promoted_public` | Passed all three gates; included in export |
| `rejected_archived` | Failed one or more gates; archived with documented reason |
| `needs_external_public_sources` | Cannot yet be confirmed; not rejected but not promoted |
| `merged_alias` | Duplicate entry; consolidated under canonical slug |
| `deferred_manual` | Requires human review; not auto-processable |

Only `promoted_public` records reach the public export.

---

## What Gets Rejected

Common rejection reasons, documented in the audit trail:

- **non_bc**: Company headquartered outside BC; Vancouver satellite of an out-of-province or international company
- **dead_domain**: Website is parked, 404, or inactive; no active social presence
- **stale_data**: Company acquired, dissolved, or wound down since the source data was captured
- **no_ai_relevance**: No AI, ML, or advanced technology product found in any public source
- **duplicate**: Same organization listed under multiple names or slugs
- **not_an_org**: Entry resolves to a personal profile, event, or non-organizational entity

---

## Public Export Filtering

The public export (`bc-ai-directory-public-v1`) applies additional safety filtering beyond the promotion gate:

- **Unsafe content removed**: Summaries are scanned and stripped of content that could identify private individuals, contact details, or sensitive organizational information
- **Incomplete records withheld**: Organizations or people missing required fields (name, summary) are held back until profiles are complete
- **Non-public flags respected**: Profiles marked `public_profile: false` are withheld even if validated

---

## Known Limitations

- This dataset reflects validation as of the release date. Organizations change — they get acquired, pivot, or dissolve. We aim to update quarterly.
- The validation process is thorough but not infallible. One false-positive (Vista Centre, a record incorrectly marked validated while its own summary noted no company was found) was caught and removed in pre-launch audit.
- ~884 organizations are in `needs_external_public_sources` state — they exist in our pipeline but have not yet been validated. They are not in this dataset.

---

## Rejection Archive

All rejected organizations are archived in the BC + AI Ecosystem Association's internal knowledge base with documented rejection reasons. This audit trail is maintained for transparency and to prevent the same organizations from being re-submitted without new evidence.

---

## Data Sources

Initial candidate pool drawn from:
- BC tech and AI company databases (Crunchbase, PitchBook, LinkedIn)
- BCTech member directory
- Event attendance and speaker data (Luma, 1,700+ event records)
- Public sector BC AI funding announcements
- Partner organization referrals
- Competitive directory cross-reference (including AI Network of BC / PAINBC)
- BC AI Ecosystem Atlas project archives
