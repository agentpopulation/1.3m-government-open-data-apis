## Government open data API endpoints, snapshot 15 Nov 2026

- 1,329,192 endpoints passed a keyless data call, tested 10–15 Nov 2026 (IST)
- 57,593 services · 250 country codes · 1,008,314 keyless JSON rows

### Download

- `Government_Open_Data_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz`: the full list, 1,329,192 rows, 52.2 MB gzipped (423.3 MB as CSV), SHA-256 `b4affa803ef59cb7241f5e8b656a860b0ed3d2870315a6086ee0fbc41ab60625`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Government_Open_Data_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Government_Open_Data_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 120,356 · Wrap one portal as a get_city_records tool: pass the dataset id and a filter ($where on Socrata, where on Opendatasoft, q on CKAN), return the matching records with a timeout.
- 📱 App features: 27,403 · Show the schools, parks, libraries or fire and police stations near an address on a map card; each layer query returns features with names and attributes.
- 🧠 Grounding and data pipelines: 311,011 · Load municipal and national files on a schedule into your own store, keeping the portal and dataset id, so answers about a city cite a dated public record.
- 🧪 Evals and testing: 1,329,192 · Run your civic-data tool against a fixed set of URLs across portals and formats; check that records, fields and dates parse, and keep last_tested as the baseline for your own re-tests.

### Changes

- First release
- Left out: 1,161 rows whose URL carried a credential-looking parameter or a login.
- Left out: 2 rows with a private or local address.
- Left out: 10 rows with an email-like address.
- Left out: 29,696 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 11 camera or image URLs (webcam and camera feeds, picture and video files).
- Left out: 49 class-exercise copies of the same few ArcGIS Online layers (Miami Beach sea level rise, high-risk areas without shelter, flooded areas, sea level rise and storm surge maps) across many organisations, many with a person's name in the title.
- Left out: 273 layers marked editable in the title (they can hold entries that people added).
- Left out: 5,340 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 18 rows that passed a data call only from a network location in India.
- Left out: 5,173 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 947 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 102,904 rows of server information from Mastodon, PeerTube, Lemmy, Nostr and other social network servers (instance documents name the server's contact person).
- Left out: 1 row that repeats an address already in the pack.
- Overlap: 4,943 of these URLs are also in 190k-weather-apis-for-agents.
- Overlap: 22,366 of these URLs are also in 270k-transit-apis-for-agents.
- Overlap: 2,525 of these URLs are also in 270k-water-apis-for-agents.
- Overlap: 8,283 of these URLs are also in 130k-finance-economy-apis-for-agents.
- Overlap: 5,038 of these URLs are also in 130k-india-apis-for-agents.
- Overlap: 1,157 of these URLs are also in 86k-oceans-apis-for-agents.
- Overlap: 365 of these URLs are also in 20k-air-quality-apis-for-agents.
- Overlap: 1,008,314 of these URLs are also in 2.5m-agent-ready-apis.
- Overlap: 85 of these URLs are also in 6.5k-wildfire-apis-for-agents.
- Overlap: 199 of these URLs are also in 24k-traffic-apis-for-agents.
- Overlap: 846 of these URLs are also in 12k-parking-apis-for-agents.
- Overlap: 160 of these URLs are also in 10k-earthquake-apis-for-agents.
- Overlap: 115 of these URLs are also in 5.2k-volcano-tsunami-apis-for-agents.
- Overlap: 26 of these URLs are also in 17k-bike-share-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 10–15 Nov 2026; snapshot 15 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 15 Nov 2026.

Credit: Government open data API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 15 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
