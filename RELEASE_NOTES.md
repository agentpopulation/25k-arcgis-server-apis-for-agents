## ArcGIS Server API endpoints, snapshot 16 Nov 2026

- 25,292 endpoints passed a keyless data call, tested 16 Nov 2026 (IST)
- 1,306 services · 51 country codes · 25,292 keyless JSON rows

### Download

- `ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz`: the full list, 25,292 rows, 440.8 kB gzipped (6.9 MB as CSV), SHA-256 `775f25e39b03c4c76b9fb39ce82a200f5b99b3eda29e3a2c3f8cf2434a082733`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 25,292 · Wrap one layer query as a get_layer_features tool: pass a where clause or a bounding box, return the matching features with a timeout.
- 📱 App features: 25,292 · Add the layers to an app map: read the layer once for its fields, then ask for the features in the visible area.
- 🧠 Grounding and data pipelines: 2,570 · Load the tables and layers on a schedule into your own store, so an agent can cite a dated source.
- 🧪 Evals and testing: 25,292 · Run your tool calls against a fixed set of URLs across formats and record which answer; last_tested is the baseline for your own re-tests.

### Changes

- First release
- Left out: 1 row with an email-like address.
- Left out: 3 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 7 layers marked editable in the title (they can hold entries that people added).
- Left out: 9 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 42 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 22 ArcGIS layers that are records about named people (employee, patient, client or donor lists, home addresses, voter lists, sex offender and missing person layers).
- Left out: 458 rows of university, college and school organisations and hosts (many of their layers are students' work).
- Left out: 4,376 rows that are another address form of an ArcGIS layer already in an earlier pack of the collection (the same rows under another query).
- Overlap: 11,583 of these URLs are also in 750k-united-states-apis-for-agents.
- Overlap: 315 of these URLs are also in 52k-united-kingdom-apis-for-agents.
- Overlap: 42 of these URLs are also in 47k-france-apis-for-agents.
- Overlap: 177 of these URLs are also in 8.1k-spain-apis-for-agents.
- Overlap: 3 of these URLs are also in 22k-indonesia-apis-for-agents.
- Overlap: 931 of these URLs are also in 19k-canada-apis-for-agents.
- Overlap: 110 of these URLs are also in 17k-netherlands-apis-for-agents.
- Overlap: 1,132 of these URLs are also in 14k-germany-apis-for-agents.
- Overlap: 296 of these URLs are also in 12k-norway-apis-for-agents.
- Overlap: 854 of these URLs are also in 14k-brazil-apis-for-agents.
- Overlap: 9 of these URLs are also in 9.8k-japan-apis-for-agents.
- Overlap: 52 of these URLs are also in 12k-australia-apis-for-agents.
- Overlap: 716 of these URLs are also in 10k-colombia-apis-for-agents.
- Overlap: 62 of these URLs are also in 6.3k-czechia-apis-for-agents.
- Overlap: 14 of these URLs are also in 6.3k-poland-apis-for-agents.
- Overlap: 59 of these URLs are also in 7.3k-italy-apis-for-agents.
- Overlap: 255 of these URLs are also in 6.1k-new-zealand-apis-for-agents.
- Overlap: 407 of these URLs are also in 13k-nordic-apis-for-agents.
- Overlap: 1,708 of these URLs are also in 24k-more-europe-apis-for-agents.
- Overlap: 598 of these URLs are also in 20k-latin-america-caribbean-apis-for-agents.
- Overlap: 197 of these URLs are also in 6.7k-middle-east-africa-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 16 Nov 2026; snapshot 16 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 16 Nov 2026.

Credit: ArcGIS Server API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 16 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
