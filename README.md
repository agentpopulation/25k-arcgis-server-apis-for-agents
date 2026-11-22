<p align="center"><img src="assets/banner.svg" width="100%" alt="ArcGIS Server API endpoints: 25,292 API endpoints passed a keyless data call"></p>

# 🖥️ ArcGIS Server API endpoints

**25,292 ArcGIS Server API endpoints that answered a keyless GET with a data body. For agent and app builders.**

<p align="center"><a href="#files"><img src="https://img.shields.io/badge/endpoints-25%2C292-6366F1" alt="endpoints: 25,292"></a> <a href="#columns-and-tags"><img src="https://img.shields.io/badge/keyless%20JSON-25%2C292-6366F1" alt="keyless JSON: 25,292"></a> <a href="#whats-inside"><img src="https://img.shields.io/badge/services-1%2C306-0F172A" alt="services: 1,306"></a> <a href="#whats-inside"><img src="https://img.shields.io/badge/country%20codes-51-EA580C" alt="country codes: 51"></a> <a href="LICENSE"><img src="https://img.shields.io/badge/licence-CC%20BY%204.0-0F172A" alt="licence: CC BY 4.0"></a></p>

<p align="center"><a href="#whats-in-it-for-you">What's in it</a> · <a href="#for-ai-agents">For AI agents</a> · <a href="#quick-start">Quick start</a> · <a href="#test-it-yourself">Test it yourself</a> · <a href="#files">Files</a> · <a href="#licence-and-credit">Licence</a> · <a href="#part-of-10m-api-endpoints-for-ai-agents">More packs</a></p>

This repository holds a 1,000-row sample and the services list; the full list of 25,292 endpoints is one download from the [latest release](https://github.com/agentpopulation/25k-arcgis-server-apis-for-agents/releases/latest).

**Endpoints for building a map tool on organisations' own map servers.** Feature and map layers served by organisations' own ArcGIS servers (agencies, cities, regional councils, engineering firms), not hosted on ArcGIS Online, as URLs that answered with no key on their test date.

Selection rule: rows where `url contains "/rest/services/" AND NOT host ends with "arcgis.com"`, less the rows that a leave-out rule drops (each counted under Known limits).

24,616 of these 25,292 rows match the focus rule (below); the others are in the pack by the selection rule only, and Known limits says what they are.

## In plain words

**What is an API endpoint?** An API endpoint is one web address that a program can ask for data, for example the latest reading at one weather station. A single service, such as a national weather agency, can have thousands of endpoints: one per station, city or dataset. This pack counts endpoints, not separate services.

**What does "passed a data call" mean?** On the date shown in each row, AgentPopulation sent one plain request to that address, with no password or key, and got a non-empty data body back (JSON, CSV, XML or a file): not an error page and not an empty result. Some bodies describe a dataset rather than hold its values; see Known limits. It shows the address answered with data on that day. It is not a promise that it answers today, and licences and usage limits were not reviewed.

## What's in it for you

Four ways to use this pack. Each bucket gives a count, a filter you can apply to the CSV, one example that passed, and a list of recommended starting points with the rule that picked them. Buckets overlap; a row can fit more than one.

Examples, recommended lists and the preview are drawn from rows that match this pack's focus rule, so a row that the selection rule put in this pack but that is about something else is not shown as a starting point. Counts cover the whole bucket.

<details>
<summary>The focus rule</summary>

Focus rule: `NOT title matches /(?<![a-z])(test|tests|testing|draft|drafts|copy|sample|samples|demo|untitled|scratch|temp|tmp|delete|deleteme|practice|dummy|example|training)(?![a-z])|final_final|\d{7,}/i AND (NOT url matches ///(services[0-9]*(-[a-z0-9]+)?|utility)\.arcgis\.com//i OR NOT service matches /^ArcGIS organization /i)`

</details>

### 🤖 Agent tools: Keyless JSON layers and tables an agent can call (ArcGIS Server)

**25,292** endpoints from 1,306 services · Wrap one layer query as a get_layer_features tool: pass a where clause or a bounding box, return the matching features with a timeout.

25,292 of these are map-layer queries that asked for a few records (`resultRecordCount`); add a where clause or a geometry to ask about one place, and page through for the whole layer.

Start with: `tags has agent-ready`

Example: [EDXSpatialCaches/AMLIS\_Problem\_Area\_2025](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) · Doe · passed 2026-11-16

<details>
<summary>Recommended starting points: 8 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack with the most endpoints that match this bucket and are tagged `agent-ready` (no key sent in the test call, JSON body, passed a data call). Ties go to the service with more country codes, then by name. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Sample preference in this bucket: `url matches //query\?/i`. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Doe (prod.arcgis.netl.doe.gov) | 1,349 | 1,349 | US | json | [EDXSpatialCaches/AMLIS\_Problem\_Area\_2025](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| app2.ge.ch | 1,144 | 1,144 | CH | json | [Hosted/AGGLO\_AIRE\_URB](https://app2.ge.ch/tergeoservices/rest/services/Hosted/AGGLO_AIRE_URB/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Nrw (www.arcgishostedserver.nrw.de) | 954 | 954 | DE | json | [Hosted/Änderung\_Gewerbesteuer\_Ist\_Aufko…](https://www.arcgishostedserver.nrw.de/arcgis/rest/services/Hosted/%C3%84nderung_Gewerbesteuer_Ist_Aufkommen_2020_zu_2019_in_Prozent/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Debristech (gis1.debristech.com) | 587 | 587 | global or unknown | json | [DebrisProjects/DT385\_Tree](https://gis1.debristech.com/arcgis/rest/services/DebrisProjects/DT385_Tree/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Cordoba (gis.cordoba.gob.ar) | 332 | 332 | AR | json | [Ambiente/Plan\_Forestal\_pb](https://gis.cordoba.gob.ar/server/rest/services/Ambiente/Plan_Forestal_pb/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Nctcog (geospatial.nctcog.org) | 303 | 303 | global or unknown | json | [Hosted/14\_18\_PSAP\_Grid\_nozero](https://geospatial.nctcog.org/server/rest/services/Hosted/14_18_PSAP_Grid_nozero/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Fehrandpeers (devapps.fehrandpeers.com) | 285 | 285 | global or unknown | json | [2045\_RIVCOM\_Links](https://devapps.fehrandpeers.com/devgis/rest/services/2045_RIVCOM_Links/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Ibama (pamgia.ibama.gov.br) | 256 | 256 | BR | json | [21\_SIGA\_Geo/duto](https://pamgia.ibama.gov.br/server/rest/services/21_SIGA_Geo/duto/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

### 📱 App features: Map layers to draw in an app (ArcGIS Server)

**25,292** endpoints from 1,306 services · Add the layers to an app map: read the layer once for its fields, then ask for the features in the visible area.

Start with: `url matches //(Feature|Map)Server//i`

Example: [EDXSpatialCaches/AMLIS\_Problem\_Area\_2025](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) · Doe · passed 2026-11-16

<details>
<summary>Recommended starting points: 8 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack with the most endpoints that match this bucket and passed a data call. Ties go to the service with more country codes, then by name. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Doe (prod.arcgis.netl.doe.gov) | 1,349 | 1,349 | US | json | [EDXSpatialCaches/AMLIS\_Problem\_Area\_2025](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| app2.ge.ch | 1,144 | 1,144 | CH | json | [Hosted/AGGLO\_AIRE\_URB](https://app2.ge.ch/tergeoservices/rest/services/Hosted/AGGLO_AIRE_URB/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Nrw (www.arcgishostedserver.nrw.de) | 954 | 954 | DE | json | [Hosted/Änderung\_Gewerbesteuer\_Ist\_Aufko…](https://www.arcgishostedserver.nrw.de/arcgis/rest/services/Hosted/%C3%84nderung_Gewerbesteuer_Ist_Aufkommen_2020_zu_2019_in_Prozent/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Debristech (gis1.debristech.com) | 587 | 587 | global or unknown | json | [DebrisProjects/DT385\_Tree](https://gis1.debristech.com/arcgis/rest/services/DebrisProjects/DT385_Tree/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Cordoba (gis.cordoba.gob.ar) | 332 | 332 | AR | json | [Ambiente/Plan\_Forestal\_pb](https://gis.cordoba.gob.ar/server/rest/services/Ambiente/Plan_Forestal_pb/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Nctcog (geospatial.nctcog.org) | 303 | 303 | global or unknown | json | [Hosted/14\_18\_PSAP\_Grid\_nozero](https://geospatial.nctcog.org/server/rest/services/Hosted/14_18_PSAP_Grid_nozero/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Fehrandpeers (devapps.fehrandpeers.com) | 285 | 285 | global or unknown | json | [2045\_RIVCOM\_Links](https://devapps.fehrandpeers.com/devgis/rest/services/2045_RIVCOM_Links/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Ibama (pamgia.ibama.gov.br) | 256 | 256 | BR | json | [21\_SIGA\_Geo/duto](https://pamgia.ibama.gov.br/server/rest/services/21_SIGA_Geo/duto/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

### 🧠 Grounding and data pipelines: Statistics, boundaries, parcels and inventories for scheduled loads (ArcGIS Server)

**2,570** endpoints from 625 services · Load the tables and layers on a schedule into your own store, so an agent can cite a dated source.

Start with: `format in (csv, xml, geojson) OR title matches /statist|census|population|boundar|parcel|zoning|district|budget|election|crash|permit|inventory|land ?use|landuse|cadast|address/i`

Example: [ServicesBoone/CountyCommissionerDistrictsLabelsLa…](https://secure.boonecountygis.com/server/rest/services/ServicesBoone/CountyCommissionerDistrictsLabelsLayer_Boone/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) · Boonecountygis · passed 2026-11-16

<details>
<summary>Recommended starting points: 8 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack with the most endpoints that match this bucket and passed a data call. Ties go to the service with more country codes, then by name. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Boonecountygis (secure.boonecountygis.com) | 57 | 153 | US | json | [ServicesBoone/CountyCommissionerDistric…](https://secure.boonecountygis.com/server/rest/services/ServicesBoone/CountyCommissionerDistrictsLabelsLayer_Boone/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Nctcog (geospatial.nctcog.org) | 56 | 303 | global or unknown | json | [Hosted/2015\_2019\_Non\_Fatal\_Bicyle\_Crash](https://geospatial.nctcog.org/server/rest/services/Hosted/2015_2019_Non_Fatal_Bicyle_Crash/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Debristech (gis1.debristech.com) | 45 | 587 | global or unknown | json | [Hosted/BatesvilleMS\_Boundary](https://gis1.debristech.com/arcgis/rest/services/Hosted/BatesvilleMS_Boundary/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Bostonplans (gis.bostonplans.org) | 44 | 81 | global or unknown | json | [Assessing\_Parcels\_20\_for\_BOLD](https://gis.bostonplans.org/hosting/rest/services/Assessing_Parcels_20_for_BOLD/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Sgrcmaps (www.sgrcmaps.com) | 44 | 130 | global or unknown | json | [Atkinson/Addresses](https://www.sgrcmaps.com/alma/rest/services/Atkinson/Addresses/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Eaglecounty (map.eaglecounty.us) | 34 | 114 | US | json | [2026\_Address\_Points](https://map.eaglecounty.us/arcgiswa/rest/services/2026_Address_Points/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Fehrandpeers (devapps.fehrandpeers.com) | 31 | 285 | global or unknown | json | [City\_Boundary\_Web\_Map](https://devapps.fehrandpeers.com/devgis/rest/services/City_Boundary_Web_Map/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Doe (prod.arcgis.netl.doe.gov) | 25 | 1,349 | US | json | [EDXSpatialCaches/MorganCountyParcels\_UT…](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/MorganCountyParcels_UTM15N_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

### 🧪 Evals and testing: Varied responses to test tool calls and parsers

**25,292** endpoints · 1,306 services · 51 country codes · 1 format · Run your tool calls against a fixed set of URLs across formats and record which answer; last_tested is the baseline for your own re-tests.

Start with: the whole pack

Example: [EDXSpatialCaches/AMLIS\_Problem\_Area\_2025](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) · Doe · passed 2026-11-16

<details>
<summary>Recommended starting points: 8 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack that returned the most different formats, then the most endpoints that passed a data call, then by name: a mix of response shapes to test parsers and tool calls. Here the services returned 1 format each, so the order comes down to endpoint counts. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Doe (prod.arcgis.netl.doe.gov) | 1,349 | 1,349 | US | json | [EDXSpatialCaches/AMLIS\_Problem\_Area\_2025](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| app2.ge.ch | 1,144 | 1,144 | CH | json | [Hosted/AGGLO\_AIRE\_URB](https://app2.ge.ch/tergeoservices/rest/services/Hosted/AGGLO_AIRE_URB/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Nrw (www.arcgishostedserver.nrw.de) | 954 | 954 | DE | json | [Hosted/Änderung\_Gewerbesteuer\_Ist\_Aufko…](https://www.arcgishostedserver.nrw.de/arcgis/rest/services/Hosted/%C3%84nderung_Gewerbesteuer_Ist_Aufkommen_2020_zu_2019_in_Prozent/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Debristech (gis1.debristech.com) | 587 | 587 | global or unknown | json | [DebrisProjects/DT385\_Tree](https://gis1.debristech.com/arcgis/rest/services/DebrisProjects/DT385_Tree/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Cordoba (gis.cordoba.gob.ar) | 332 | 332 | AR | json | [Ambiente/Plan\_Forestal\_pb](https://gis.cordoba.gob.ar/server/rest/services/Ambiente/Plan_Forestal_pb/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Nctcog (geospatial.nctcog.org) | 303 | 303 | global or unknown | json | [Hosted/14\_18\_PSAP\_Grid\_nozero](https://geospatial.nctcog.org/server/rest/services/Hosted/14_18_PSAP_Grid_nozero/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Fehrandpeers (devapps.fehrandpeers.com) | 285 | 285 | global or unknown | json | [2045\_RIVCOM\_Links](https://devapps.fehrandpeers.com/devgis/rest/services/2045_RIVCOM_Links/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Ibama (pamgia.ibama.gov.br) | 256 | 256 | BR | json | [21\_SIGA\_Geo/duto](https://pamgia.ibama.gov.br/server/rest/services/21_SIGA_Geo/duto/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

The same lists are in [recommended.json](recommended.json), ready for an agent to load.

## Questions an agent can answer with this pack

- Which layers does the canton of Geneva serve from its own server? Try [Hosted/AGGLO\_AIRE\_URB](https://app2.ge.ch/tergeoservices/rest/services/Hosted/AGGLO_AIRE_URB/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (app2.ge.ch, passed 2026-11-16).
- Which layers does the North Central Texas Council of Governments serve? Try [Hosted/14\_18\_PSAP\_Grid\_nozero](https://geospatial.nctcog.org/server/rest/services/Hosted/14_18_PSAP_Grid_nozero/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (Nctcog, passed 2026-11-16).
- Which hosted layers does North Rhine-Westphalia serve from its own server? Try [Hosted/Änderung\_Gewerbesteuer\_Ist\_Aufkommen\_2020\_…](https://www.arcgishostedserver.nrw.de/arcgis/rest/services/Hosted/%C3%84nderung_Gewerbesteuer_Ist_Aufkommen_2020_zu_2019_in_Prozent/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (Nrw, passed 2026-11-16).

## What "passed a data call" means

> [!NOTE]
> On the date in `last_tested` (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The `format` column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 16 Nov 2026; snapshot 16 Nov 2026.

## For AI agents

Start from keyless JSON endpoints (`agent-ready`). The code below loads `recommended.json` and calls the first recommended service in the Agent tools bucket, with a timeout (`node examples/agent-start.mjs --recommended`). With no argument, `node examples/agent-start.mjs` calls the most recently tested agent-ready row of the sample; pass a `.csv` or `.csv.gz` path to use that file instead. See [examples/agent-start.mjs](examples/agent-start.mjs).

```js
// Node 18+. Loads recommended.json (the local copy, or the raw file on GitHub) and calls one keyless JSON endpoint.
import fs from 'node:fs';

const RAW = 'https://raw.githubusercontent.com/agentpopulation/25k-arcgis-server-apis-for-agents/main/recommended.json';
const rec = fs.existsSync('recommended.json')
  ? JSON.parse(fs.readFileSync('recommended.json', 'utf8'))
  : await (await fetch(RAW)).json();

const pick = rec.buckets.find((b) => b.id === 'agent').services[0];
try {
  const res = await fetch(pick.sample_url, {
    headers: { 'User-Agent': 'agent-example/1.0' },
    signal: AbortSignal.timeout(15000),
  });
  console.log(pick.service, res.status, res.headers.get('content-type'));
  console.log((await res.text()).slice(0, 300));
} catch (err) {
  console.log(`did not answer now; last passed ${pick.sample_last_tested} (${err.message})`);
}
```

How an agent picks an endpoint:

1. Filter to `agent-ready` and your country or topic.
2. Prefer the newest `last_tested` and the larger services.
3. Call with a timeout and check the body before you use it.

## Quick start

The examples run against the sample in `data/` out of the box (1,000 rows). Each takes an optional path to a `.csv` or `.csv.gz` file instead.

```bash
git clone https://github.com/agentpopulation/25k-arcgis-server-apis-for-agents.git
cd 25k-arcgis-server-apis-for-agents
python examples/quickstart.py
node examples/quickstart.mjs
node examples/agent-start.mjs
```

Full list: download `ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz` (25,292 rows, 440.8 kB) from [releases/latest](https://github.com/agentpopulation/25k-arcgis-server-apis-for-agents/releases/latest), then gunzip it and pass its path. The scripts also read the `.csv.gz` as it is.

```bash
gunzip ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz
python examples/quickstart.py ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv
node examples/quickstart.mjs ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv
```

### curl

Quote the URL: some contain commas.

```bash
curl -sL "https://raw.githubusercontent.com/agentpopulation/25k-arcgis-server-apis-for-agents/main/data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.csv" | head -n 4
curl -s --max-time 15 "https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json" | head -c 600
```

### Python

Standard library only: [examples/quickstart.py](examples/quickstart.py) reads the sample, or the path you pass, keeps agent-ready rows and calls the most recently tested one.

<details>
<summary>The code</summary>

```python
# Python 3, standard library only. Run from a clone of this repository:
#   python examples/quickstart.py [path]
# With no path it reads the sample in data/. Pass the full list from the latest release (.csv or .csv.gz) instead.
# Keeps agent-ready rows and calls the most recently tested one.
import csv
import gzip
import os
import re
import sys
import urllib.request

HERE = os.path.dirname(os.path.abspath(__file__))
path = sys.argv[1] if len(sys.argv) > 1 else os.path.join(HERE, "..", "data", "ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.csv")
opener = gzip.open if path.endswith(".gz") else open
with opener(path, "rt", newline="", encoding="utf-8") as f:
    rows = list(csv.DictReader(f))

agent = [r for r in rows if "agent-ready" in r["tags"].split("|")]
# Newest test date first; URLs that describe a dataset or a service rather than return values go last.
DESCRIBES = re.compile(r"/erddap/info/|action-report\.json$|[?&]request=getcapabilities|/GeoArea/[^/?]+/List|getFullTableDownloadCSV|hub\.worldpop\.org", re.I)
agent.sort(key=lambda r: r["last_tested"], reverse=True)
agent.sort(key=lambda r: 1 if DESCRIBES.search(r["url"]) else 0)
print(len(rows), "rows,", len(agent), "agent-ready")
if not agent:
    sys.exit(0)

row = agent[0]
req = urllib.request.Request(row["url"], headers={"User-Agent": "agent-example/1.0"})
try:
    with urllib.request.urlopen(req, timeout=15) as res:
        body = res.read(1_000_000).decode("utf-8", "replace")
        print(res.status, res.headers.get("Content-Type"))
        print(body[:300])
except Exception as err:
    print(f"did not answer now; last passed {row['last_tested']} ({err})")
```

</details>

### JavaScript

Reads the sample as JSON because the CSV has quoted commas.

<details>
<summary>The code</summary>

```js
// Node 18+. Reads the sample as JSON (the CSV has quoted commas), local file first.
import fs from 'node:fs';

const FILE = 'data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.json';
const rows = fs.existsSync(FILE)
  ? JSON.parse(fs.readFileSync(FILE, 'utf8'))
  : await (await fetch('https://raw.githubusercontent.com/agentpopulation/25k-arcgis-server-apis-for-agents/main/data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.json')).json();

const row = rows.find((r) => r.tags.includes('agent-ready'));
const res = await fetch(row.url, { headers: { 'User-Agent': 'agent-example/1.0' }, signal: AbortSignal.timeout(15000) });
console.log(res.status, (await res.text()).slice(0, 300));
```

</details>

### Agent tools

[examples/agent-tools.json](examples/agent-tools.json) holds two tool definitions in the shape most tool-calling APIs accept (name, description, JSON Schema); rename `parameters` if yours uses another key. [examples/quickstart.mjs](examples/quickstart.mjs) implements them:

- `find_endpoints` searches the agent-ready rows of the list by words, country code (their format is json). When you load the tools of more than one pack, prefix the names (for example `arcgis_server_find_endpoints`) so they do not clash.
- `fetch_endpoint` calls one URL, **refuses any URL that is not in the list** and does not follow redirects. The allowlist is built from the CSV, so a URL injected into a prompt is refused.

The same two tools can sit behind an MCP server.

## Test it yourself

Re-test endpoints from the sample with the same rule: HTTP 2xx and a non-empty body that is not an HTML page. Node 18+, no packages.

```bash
node tools/test-endpoints.mjs
```

It tests the first 50 URLs and prints one line: tested, passed, did not pass. Options: a `.csv` or `.csv.gz` path (the full list from the release), `--limit 50`, `--timeout-ms 10000`, `--out results.csv`. The results file holds `url`, `status`, `passed`, `content_type`, `ms` and `checked_at`; a status of `timeout` or `error:<code>` means no HTTP answer came back. It is polite: GET only, no key sent, at most 4 requests in flight, one at a time per listed host, at least 1 second between requests to one listed host, and reading stops once 256 kB of a body is kept. Redirects are followed and may lead to another host. `results.csv` is in `.gitignore`.

## Preview

One row from each of the five largest services among rows that match the focus rule, services with rows that return values first.

| Title | Service | Country | Format | Tested | Link |
|---|---|---|---|---|---|
| EDXSpatialCaches/AMLIS\_Problem\_Area\_2025 | Doe | US | json | 2026-11-16 | [prod.arcgis.netl.doe.gov](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |
| Hosted/AGGLO\_AIRE\_URB | app2.ge.ch | CH | json | 2026-11-16 | [app2.ge.ch](https://app2.ge.ch/tergeoservices/rest/services/Hosted/AGGLO_AIRE_URB/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |
| Hosted/Änderung\_Gewerbesteuer\_Ist\_Aufkommen\_2020\_zu\_2019\_in… | Nrw | DE | json | 2026-11-16 | [www.arcgishostedserver.nrw.de](https://www.arcgishostedserver.nrw.de/arcgis/rest/services/Hosted/%C3%84nderung_Gewerbesteuer_Ist_Aufkommen_2020_zu_2019_in_Prozent/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |
| DebrisProjects/DT385\_Tree | Debristech | global or unknown | json | 2026-11-16 | [gis1.debristech.com](https://gis1.debristech.com/arcgis/rest/services/DebrisProjects/DT385_Tree/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |
| Ambiente/Plan\_Forestal\_pb | Cordoba | AR | json | 2026-11-16 | [gis.cordoba.gob.ar](https://gis.cordoba.gob.ar/server/rest/services/Ambiente/Plan_Forestal_pb/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |

Browse the 1,000-row sample: [Sample CSV](data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.csv) · [Sample JSON](data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.json).

## What's inside

<p align="center"><img src="assets/breakdown.svg" width="100%" alt="Top categories and formats in this pack"></p>

<details>
<summary>Country codes: 51</summary>

| Code | Country | Endpoints | |
|---|---|---:|---|
| US | United States | 11,583 | `████████████████████` |
| CH | Switzerland | 1,316 | `██▎` |
| DE | Germany | 1,132 | `██` |
| CA | Canada | 931 | `█▋` |
| BR | Brazil | 854 | `█▌` |
| CO | Colombia | 716 | `█▎` |
| AR | Argentina | 333 | `▋` |
| GB | United Kingdom | 315 | `▌` |
| NO | Norway | 296 | `▌` |
| NZ | New Zealand | 255 | `▌` |
| | other 41 codes | 2,040 | |
| | global or unknown | 5,521 | `█████████▌` |

</details>

<details>
<summary>Categories: top 8</summary>

| Category | Endpoints | |
|---|---:|---|
| Navigation & Geo/Maps | 17,834 | `████████████████████` |
| Government & Open Data | 2,079 | `██▍` |
| Transport & Mobility | 1,919 | `██▏` |
| Environment | 1,041 | `█▏` |
| Hydrology & Oceans | 827 | `▉` |
| Health | 433 | `▌` |
| Weather & Climate | 373 | `▍` |
| Hazards | 363 | `▍` |

</details>

Formats: json 25,292

<details>
<summary>Largest services: top 25 of 1,306</summary>

| Service | Host | Endpoints | Keyless JSON | |
|---|---|---:|---:|---|
| Doe | prod.arcgis.netl.doe.gov | 1,349 | 1,349 | `████████████████████` |
| app2.ge.ch | app2.ge.ch | 1,144 | 1,144 | `█████████████████` |
| Nrw | www.arcgishostedserver.nrw.de | 954 | 954 | `██████████████▏` |
| Debristech | gis1.debristech.com | 587 | 587 | `████████▊` |
| Cordoba | gis.cordoba.gob.ar | 332 | 332 | `████▉` |
| Nctcog | geospatial.nctcog.org | 303 | 303 | `████▌` |
| Fehrandpeers | devapps.fehrandpeers.com | 285 | 285 | `████▎` |
| Ibama | pamgia.ibama.gov.br | 256 | 256 | `███▊` |
| sinfor.marica.rj.gov.br | sinfor.marica.rj.gov.br | 225 | 225 | `███▍` |
| Noaa | imagery.coast.noaa.gov | 223 | 223 | `███▎` |
| Noaa | maps1.coast.noaa.gov | 223 | 223 | `███▎` |
| Noaa | maps2.coast.noaa.gov | 221 | 221 | `███▎` |
| Prosperidadsocial | gis.prosperidadsocial.gov.co | 191 | 191 | `██▉` |
| Civilsolutions | ags.civilsolutions.biz | 188 | 188 | `██▊` |
| mapas.conder.ba.gov.br | mapas.conder.ba.gov.br | 185 | 185 | `██▊` |
| Igac | mapas.igac.gov.co | 183 | 183 | `██▊` |
| Thorntonco | maps.thorntonco.gov | 175 | 175 | `██▋` |
| gis.ecology.wa.gov | gis.ecology.wa.gov | 162 | 162 | `██▍` |
| Codot | maps.codot.gov | 158 | 158 | `██▍` |
| Boonecountygis | secure.boonecountygis.com | 153 | 153 | `██▎` |
| Superservicios | geoportal.superservicios.gov.co | 149 | 149 | `██▎` |
| arcgis.cetesb.sp.gov.br | arcgis.cetesb.sp.gov.br | 145 | 145 | `██▏` |
| Unibe | gis.cde.unibe.ch | 143 | 143 | `██▏` |
| Semcog | gis.semcog.org | 141 | 141 | `██▏` |
| Sandiego | webmaps.sandiego.gov | 139 | 139 | `██` |

</details>

<details>
<summary>Rows per test date: 16 Nov 2026</summary>

| Date (IST) | Endpoints | |
|---|---:|---|
| 2026-11-16 | 25,292 | `████████████████████` |

</details>

## Files

| File | Rows | Size | Use |
|---|---:|---:|---|
| [data/ArcGIS_Server_API_Services_AgentPopulation.csv](data/ArcGIS_Server_API_Services_AgentPopulation.csv) | 1,306 | 49.0 kB | One row per service with its endpoint count in this pack |
| [data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.csv](data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.csv) | 1,000 | 273.2 kB | The sample: focus-rule rows first, each service in proportion to its share; ArcGIS Online layers count as one service |
| [data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.json](data/ArcGIS_Server_API_Endpoints_AgentPopulation_Sample.json) | 1,000 | 456.2 kB | The same rows as JSON, tags as an array |
| [ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz](https://github.com/agentpopulation/25k-arcgis-server-apis-for-agents/releases/latest) | 25,292 | 440.8 kB | The full list, gzipped CSV: a download from the latest release, checked by `SHA256SUMS.txt` |
| [tools/test-endpoints.mjs](tools/test-endpoints.mjs) | | | Re-tests endpoints from the sample or the full list |

Sample size: 1,000 rows, which is 1,000 or one third of the pack rounded down, whichever is smaller. Rows that match the focus rule come first. Each service gets rows in proportion to its share of those rows, at least one for the largest services and at most 50% of the sample while other services have rows; ArcGIS Online layers count as one service, whatever their organisation. Within a service, agent-ready rows, rows that return values and the newest test dates come first, and rows are written in turn across services. Service root addresses are placed at the end of the sample.

Full list: download `ArcGIS_Server_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz` (25,292 rows, 440.8 kB) from [releases/latest](https://github.com/agentpopulation/25k-arcgis-server-apis-for-agents/releases/latest), then gunzip it and pass its path. The scripts also read the `.csv.gz` as it is.

Excel users: Data > From Text/CSV, UTF-8. Files are UTF-8 without a byte-order mark and comma-separated.

## Columns and tags

<details>
<summary>Columns, types and tags</summary>

| Column | Type | Example | Meaning |
|---|---|---|---|
| url | string | [https://prod.arcgis.netl.doe.gov/server…](https://prod.arcgis.netl.doe.gov/server/rest/services/EDXSpatialCaches/AMLIS_Problem_Area_2025/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) | The address that was tested |
| title | string | EDXSpatialCaches/AMLIS\_Problem\_Area\_2025 | Station, dataset or feed name |
| service | string | Doe | The service the endpoint belongs to; joins to the services file together with host |
| host | string | prod.arcgis.netl.doe.gov | Host name of the address |
| country | string | US | ISO 3166-1 alpha-2 code, or EU; empty when global or unknown |
| category | string | Navigation & Geo/Maps | Category of the endpoint |
| subcategory | string |  | Left empty from the 15 Nov 2026 snapshot; kept so the columns stay the same |
| format | string | json | What the test call returned: json, csv, geojson, xml, gtfs, zip, txt and so on |
| tags | string | `no-key\|json\|agent-ready` | Tags separated by \| |
| last_tested | date | 2026-11-16 | Date of the test call, YYYY-MM-DD (IST) |

| Tag | Rows | Meaning |
|---|---:|---|
| agent-ready | 25,292 | No key sent, JSON body, passed a data call on last_tested |
| json | 25,292 | Format of the body |
| no-key | 25,292 | No key was sent in the test call |

A machine-readable copy of this dictionary is in [datapackage.json](datapackage.json).

</details>

## Known limits

- 45.8% of rows carry country code US; 5,521 rows have no code (global or unknown).
- 6 rows come from PxWeb or Statistics Canada services. Some statistics endpoints return metadata or a pointer on GET; the table may need a second request or a POST.
- 25,292 rows are map-layer queries with resultRecordCount set: the tested call asked for a few records; change the query to get the full layer.
- No row is a layer on ArcGIS Online, where anyone can publish: the layers here are on their publishers' own ArcGIS Servers. Some are still tests or copies. Check the owner and the fields before you rely on one.
- 676 rows have a title that reads as a test, a draft, a copy or a sample; they are not used as starting points.
- Stations and feeds can go quiet after their test date; re-test a URL before you rely on it.
- Not in this pack: endpoints that need a key or a POST, and URLs that did not pass.
- Left out: 1 row with an email-like address.
- Left out: 3 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 7 layers marked editable in the title (they can hold entries that people added).
- Left out: 9 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 42 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 22 ArcGIS layers that are records about named people (employee, patient, client or donor lists, home addresses, voter lists, sex offender and missing person layers).
- Left out: 458 rows of university, college and school organisations and hosts (many of their layers are students' work).
- Left out: 4,376 rows that are another address form of an ArcGIS layer already in an earlier pack of the collection (the same rows under another query).

## Licence and credit

> [!IMPORTANT]
> This list (URLs, titles, tags and test results) is © 2026 AgentPopulation, released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Credit AgentPopulation and link agentpopulation.com. The data each endpoint returns belongs to its provider and stays under that provider's terms; this licence does not cover it.

Copy-ready credit:

`ArcGIS Server API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 16 Nov 2026.`

GitHub's "Cite this repository" button reads [CITATION.cff](CITATION.cff).

<!-- agentpopulation:start -->
## Part of 10M API endpoints for AI agents

This pack is one of the 50 topic packs of [10m-open-apis-for-ai-agents](https://github.com/agentpopulation/10m-open-apis-for-ai-agents), the open collection by [AgentPopulation](https://agentpopulation.com). Target: 10 million+ open API endpoints that pass a keyless API call.

AgentPopulation's test run of 16 Nov 2026: 4,452,803 tested, 3,346,053 passed a data call. This is the ArcGIS Server pack: 25,292 endpoints from 1,306 services, none of them in a pack read from the earlier snapshot, by address or as another address of the same map layer. Packs overlap, so an endpoint can appear in more than one.

For the latest tested endpoints, search [agentpopulation.com/apis](https://agentpopulation.com/apis). This pack is a snapshot from 16 Nov 2026.

Sibling packs that share the most URLs with this one: [750k-united-states-apis-for-agents](https://github.com/agentpopulation/750k-united-states-apis-for-agents) (11,583 shared) · [24k-more-europe-apis-for-agents](https://github.com/agentpopulation/24k-more-europe-apis-for-agents) (1,708 shared) · [14k-germany-apis-for-agents](https://github.com/agentpopulation/14k-germany-apis-for-agents) (1,132 shared) · [19k-canada-apis-for-agents](https://github.com/agentpopulation/19k-canada-apis-for-agents) (931 shared) · [14k-brazil-apis-for-agents](https://github.com/agentpopulation/14k-brazil-apis-for-agents) (854 shared) · [10k-colombia-apis-for-agents](https://github.com/agentpopulation/10k-colombia-apis-for-agents) (716 shared). The rest are listed in [10m-open-apis-for-ai-agents](https://github.com/agentpopulation/10m-open-apis-for-ai-agents).

Questions, pack requests, reports of endpoints that stopped answering and requests to remove a row go to [Discussions](https://github.com/agentpopulation/10m-open-apis-for-ai-agents/discussions), or to [@agentpopulation](https://x.com/agentpopulation) on X. The packs are a work in progress and corrections are welcome.

Spotted a wrong row or a dead URL? Tell us on X: [@agentpopulation](https://x.com/agentpopulation).

If this pack saved you time, a star helps others find it.

---

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · [10m-open-apis-for-ai-agents](https://github.com/agentpopulation/10m-open-apis-for-ai-agents)

<!-- agentpopulation:end -->
