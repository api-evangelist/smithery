# Smithery (smithery)

Smithery is a platform for discovering, deploying, and managing Model Context Protocol (MCP) servers and skills. It operates a public registry of community-built MCP extensions that AI agents can use to access external tools, data sources, and services, plus a Connect gateway that bundles connections in a namespace behind a single MCP endpoint at mcp.smithery.run. The platform exposes APIs for server registry browsing, server deployment, skill publishing, namespace management, scoped service tokens, connection lifecycle, trigger subscriptions, and an MCP transport endpoint for AI-agent integration.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/smithery/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/smithery/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Artificial Intelligence
- Large Language Models
- MCP
- Model Context Protocol
- AI Agents
- Developer Tools
- Registry
- Skills
- Tool Discovery

## Timestamps

- **Created:** 2025-08-19
- **Modified:** 2026-05-22

## APIs

### Smithery Platform API

The Smithery Platform API provides programmatic access to the MCP server registry and the Connect gateway. It groups 55 operations across 35 paths under eight tags (servers, skills, tools, tokens, namespaces, organizations, connect, connect.mcp), covering registry search, server CRUD, releases and runtime logs, secrets, managed domains, icon management, skill bundles, organization API keys, namespace administration, scoped service tokens, and the Connect API for managing connections, triggers, and subscriptions plus a single POST /connect/{namespace}/{connectionId}/mcp endpoint that proxies MCP streamable-HTTP traffic to upstream servers.

- **Human URL:** [https://smithery.ai/docs](https://smithery.ai/docs)
- **Base URL:** `https://api.smithery.ai`

#### Tags

- Artificial Intelligence
- MCP
- Registry
- Servers
- Skills
- Tools
- Connect
- Tokens
- Namespaces
- Organizations

#### Properties

- [Documentation](https://smithery.ai/docs)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/smithery/refs/heads/main/openapi/smithery-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/smithery/refs/heads/main/openapi/smithery-documented-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open A P I  Specification](https://smithery.ai/docs/openapi.json)
- [Open A P I  Specification](https://app.stainless.com/api/spec/documented/smithery/openapi.documented.yml)
- [llms.txt](https://smithery.ai/docs/llms.txt)
- [API Reference](https://smithery.ai/docs/api-reference)
- [JSON Schema](json-schema/smithery-server-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/smithery-skill-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/smithery-server-structure.json)
- [JSON-LD](json-ld/smithery-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/smithery-rules.yml)
- [Vocabulary](vocabulary/smithery-vocabulary.yml)
- [Plans](plans/smithery-plans-pricing.yml)
- [Rate Limits](rate-limits/smithery-rate-limits.yml)
- [Fin Ops](finops/smithery-finops.yml)
- [Postman Collection](collections/smithery-documented.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smithery-documented.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/smithery.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/smithery.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/smithery-ai)
- [GitHub Organization](https://github.com/smithery-ai)
- [Documentation](https://smithery.ai/docs)
- [C L I](https://smithery.ai/docs/concepts/cli)
- [Website](https://smithery.ai/)
- [Playground](https://smithery.ai/playground)
- [Blog](https://smithery.ai/blog)
- [Documentation](https://smithery.ai/skills)
- [Authentication](https://smithery.ai/account/api-keys)
- [SDK](https://github.com/smithery-ai/typescript-api)
- [SDK](https://github.com/smithery-ai/cli)
- [Sample Code](https://github.com/smithery-ai/smithery-cookbook)
- [Documentation](https://smithery.ai/docs/concepts/what_is_mcp)
- [Documentation](https://smithery.ai/docs/use/deep-linking)
- [Documentation](https://smithery.ai/docs/use/token-scoping)
- [Documentation](https://smithery.ai/docs/use/uplink)
- [Documentation](https://smithery.ai/docs/use/listing_your_client)
- [Documentation](https://smithery.ai/docs/build/publish)
- [Documentation](https://smithery.ai/docs/build/triggers)
- [Sample Code](https://smithery.ai/docs/cookbooks/typescript_oauth_client)
- [Integration](https://smithery.ai/docs/integrations/vercel_ai_sdk)
- [M C P Server](https://mcp.smithery.run)
- [Tools](https://github.com/smithery-ai/agent.pw)
- [M C P Server](https://github.com/smithery-ai/mouseless)
- [Tools](https://github.com/smithery-ai/mcp-to-cli)
- [Tools](https://github.com/smithery-ai/workers-biscuit)
- [Tools](https://github.com/smithery-ai/registry)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
