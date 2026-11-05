# company-registry-mcp: notes for Claude

This public repository holds only the MCP Registry metadata (`*/server.json`) for two hosted MCP servers (`uk-companies-house`, `fr-sirene`) and the workflow that publishes it. The servers themselves run as Apify Actors; their code and the source copies of these files live in a separate private repository (`registry/<actor>/server.json`).

- Publishing: `.github/workflows/publish-mcp.yml` runs on a push to `main` that changes `*/server.json`, or manually. It signs in with GitHub OIDC (no personal login, no secrets) and publishes only the servers whose `server.json` changed in that push; a manual run publishes both.
- A new version: change the file in the source repository first, copy it here, and raise `version` in `server.json`. The registry rejects a version that is already published.
- Keep the namespace `io.github.registry-desk/<actor>`. Do not add personal names, company names, emails or any secrets to this repository; it is public.
- Write in English, plainly. No made-up users, reviews or usage numbers.
