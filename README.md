# BC AI Directory — Public Dataset

**963 organizations. 833 people. Every one verified.**

This is the public, open-licensed dataset behind the [BC + AI Ecosystem Association](https://bc-ai.ca) directory. It is released under CC BY 4.0 so that researchers, journalists, developers, and community organizations can build on it freely — with attribution.

---

## What's in here

| File | Description |
|---|---|
| `data/bc-ai-directory.json` | Full versioned export (`bc-ai-directory-public-v1`) with all records |
| `data/organizations.csv` | Flat table — 963 BC AI organizations |
| `data/people.csv` | Flat table — 835 public people profiles |
| `schema/v1.md` | Field definitions, type values, array encoding |
| `METHODOLOGY.md` | How organizations are validated and what gets rejected |
| `CHANGELOG.md` | Version history |

---

## Quick stats (v1.5.0, May 2026)

- **963 organizations** across BC — Vancouver, Victoria, Kelowna, Prince George, and beyond
- **833 people** — founders, researchers, operators, policymakers
- Categories: AI/ML development, health tech, climate tech, agritech, creative tech, government/policy, research and academia, Indigenous technology
- Each organization validated against: BC organizational presence, active operations, AI/technology relevance
- Minimum 2 public sources per organization

---

## How to use it

### CSV (simplest)
```bash
# Download and explore orgs
curl -O https://raw.githubusercontent.com/WalksWithASwagger/bc-ai-directory-public/main/data/organizations.csv

# In Python
import pandas as pd
df = pd.read_csv('organizations.csv')
df['categories'] = df['categories'].str.split('|')
```

### JSON (full fidelity)
```js
const dir = JSON.parse(fs.readFileSync('data/bc-ai-directory.json', 'utf-8'));
const orgs = dir.organizations;  // array of org records
const people = dir.people;       // array of person records
```

Array fields in the CSV (categories, locations, tags, websiteUrls, roles, organizations) are pipe-separated (`|`). Split on `|` to get arrays. See `schema/v1.md` for complete field reference.

---

## What this is NOT

- Not a comprehensive list of every BC tech company — it is scoped to organizations with confirmed AI/ML/technology relevance
- Not a real-time feed — updated periodically as profiles are validated
- Not a paid or commercial directory — it is community infrastructure

---

## Attribution

**BC + AI Ecosystem Association**
[bc-ai.ca](https://bc-ai.ca)

If you build something with this data, we'd love to know about it. Open an issue or reach out.

---

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](./LICENSE)

You may use, share, adapt, and build on this dataset for any purpose — including commercial — as long as you credit the BC + AI Ecosystem Association and link back to this repository.

---

## Updates

This dataset is updated as new organizations and people are validated. To get notified of new releases, watch this repository.

To suggest a correction or addition, open an issue with:
- Organization/person name
- Public website or LinkedIn URL
- Evidence of BC presence and AI/technology relevance
