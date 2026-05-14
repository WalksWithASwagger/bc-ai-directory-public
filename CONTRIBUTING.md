# Contributing to the BC AI Directory

Thank you for helping improve this dataset. The BC + AI Ecosystem Association reviews and validates all submissions — this takes time, and not every submission will be accepted. Here's how to help effectively.

---

## How to suggest a new organization

Open a GitHub issue using the **Add Organization** template and provide:

1. **Organization name** — the official legal or trade name
2. **Website URL** — primary public website (HTTPS only)
3. **BC presence evidence** — a URL confirming a BC office, BC incorporation, or BC-based team (LinkedIn company page, About Us page, BC Corporate Registry, or Crunchbase/PitchBook with a BC address)
4. **AI/technology relevance evidence** — a URL showing they build, deploy, or provide AI/ML/advanced technology products or services (product page, GitHub repo, press article, academic publication)

**Minimum bar:** 2 public sources, confirmed BC presence, confirmed AI/tech relevance. If you can't provide both, the submission will be deferred.

---

## How to suggest a new person

Open an issue using the **Add Person** template and provide:

1. **Full name**
2. **LinkedIn URL** or public profile URL
3. **Evidence of BC-based AI/technology work** — a public article, conference talk, publication, or employer page showing they work in BC AI

People profiles require the subject's implied or explicit consent to be listed publicly. We default to listing only people who have a clear public presence in the BC AI ecosystem (speakers, founders, researchers, policy makers with public roles).

---

## How to report a data error

Open an issue using the **Data Correction** template and provide:

1. The organization or person name
2. What is incorrect
3. The correct information
4. A source URL confirming the correction

---

## What we do NOT accept

- **Out-of-province HQs**: Companies headquartered outside BC — even if they have a BC satellite office or BC clients
- **AI users, not AI builders**: Companies that merely use AI tools (Slack, Notion, etc.) but don't build or deploy AI/ML technology products
- **Defunct or dissolved**: Companies with no active web presence, dissolved BC registration, or clear evidence of shutdown
- **Government agencies**: Municipal, provincial, or federal government bodies that are procuring AI rather than building it (with narrow exceptions for entities with substantial technology development mandates)
- **Personal profiles without public presence**: People who haven't chosen to be publicly listed in a BC AI context

---

## The validation process

Every submission goes through three gates before being added:

**Gate 1 — BC Organizational Presence**
Confirmed active registration, physical address, team, or operational footprint in BC. We verify through BC Corporate Registry, LinkedIn, Crunchbase, and company websites.

**Gate 2 — Active Operations**
Verified via live domain, recent social or news activity, and no evidence of dissolution, acquisition, or wind-down.

**Gate 3 — AI / Technology Relevance**
At least one AI, machine learning, data science, or advanced technology product confirmed through public sources. Using AI tools doesn't count — building or deploying them does.

Minimum 2 public sources required per entry.

---

## How the data pipeline works

1. Submissions are reviewed and researched by BC + AI Association staff and community validators
2. Validated entries are added to our internal knowledge base (`profile.md` with `status: "validated"`)
3. A periodic export script generates the public JSON and CSV files
4. Changes are committed to this repository

Community submissions via GitHub issues are reviewed in batches, typically monthly.

---

## Bulk data corrections

If you have a list of corrections (e.g., you've identified several outdated entries), open a single issue with a table of corrections rather than one issue per entry. We'll process them in batch.

---

## License

All contributions to this dataset are released under [CC BY 4.0](./LICENSE). By submitting a correction or addition, you agree that your contribution may be incorporated into the dataset and distributed under these terms.
