# Company registry MCP servers

Registry entries for two hosted MCP servers that return company-level data from official open sources:

- `uk-companies-house`: UK Companies House free company data snapshot
- `fr-sirene`: French Sirene register

Both run as Apify Actors in Standby mode and are billed per returned company (pay per event) on the caller's Apify account. Connect with Streamable HTTP and an Apify API token as a bearer token. No data about directors or other natural persons is returned.

- https://apify.com/tormanliikenne/uk-companies-house
- https://apify.com/tormanliikenne/fr-sirene

This repository only holds the registry metadata (`server.json`) and the workflow that publishes it to the MCP Registry.
