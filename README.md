# Smithery

Smithery is a platform for discovering, deploying, and managing Model Context Protocol (MCP) servers and skills. It operates a public registry of community-built MCP extensions plus a Connect gateway that bundles all connections in a namespace behind a single MCP endpoint at `mcp.smithery.run/{namespace}`. The Smithery Platform API exposes 55 operations across 35 paths covering registry browsing, server CRUD, releases and runtime logs, secrets and managed domains, skill publishing, namespace administration, scoped service tokens, organization API keys, and the Connect lifecycle (connections, triggers, subscriptions, and an MCP streamable-HTTP transport endpoint).

> "Smithery gives agents more agency by connecting them to the outside world — search the web, query databases, control browsers, reach into business tools, and much more." — smithery.ai/docs

## APIs

| API | Description |
|-----|-------------|
| [Smithery Platform API](openapi/smithery-openapi.json) | 55 operations across 8 tags: servers (18), skills (8), connect (16), connect.mcp (1), namespaces (5), organizations (3), tokens (1), general/health (1), plus domains (2) |

## Artifacts

### OpenAPI Specifications
- [smithery-openapi.json](openapi/smithery-openapi.json) — Official Smithery Platform API (from `smithery.ai/docs/openapi.json`)
- [smithery-documented-openapi.yml](openapi/smithery-documented-openapi.yml) — Stainless-documented OpenAPI variant

### Capabilities (Naftiko, per business surface)
- [smithery-general.yaml](capabilities/smithery-general.yaml) — Health check
- [smithery-servers.yaml](capabilities/smithery-servers.yaml) — Server registry, releases, logs, secrets, icons (18 ops)
- [smithery-skills.yaml](capabilities/smithery-skills.yaml) — Skill discovery and publishing (8 ops)
- [smithery-connect.yaml](capabilities/smithery-connect.yaml) — Connection lifecycle, subscriptions, triggers (16 ops)
- [smithery-connect-mcp.yaml](capabilities/smithery-connect-mcp.yaml) — MCP streamable-HTTP transport endpoint
- [smithery-domains.yaml](capabilities/smithery-domains.yaml) — Managed custom domains
- [smithery-namespaces.yaml](capabilities/smithery-namespaces.yaml) — Namespace administration (5 ops)
- [smithery-organizations.yaml](capabilities/smithery-organizations.yaml) — Team API keys (3 ops)
- [smithery-tokens.yaml](capabilities/smithery-tokens.yaml) — Scoped service tokens

### Rules
- [smithery-rules.yml](rules/smithery-rules.yml) — Spectral ruleset for Smithery API conventions

### JSON Schema
- [smithery-server-schema.json](json-schema/smithery-server-schema.json) — MCP Server entity schema
- [smithery-skill-schema.json](json-schema/smithery-skill-schema.json) — Skill entity schema

### JSON Structure
- [smithery-server-structure.json](json-structure/smithery-server-structure.json) — MCP server object structure

### JSON-LD
- [smithery-context.jsonld](json-ld/smithery-context.jsonld) — Linked data context for MCP concepts

### Examples
- [smithery-list-servers-example.json](examples/smithery-list-servers-example.json) — List servers request/response
- [smithery-get-server-example.json](examples/smithery-get-server-example.json) — Get a server by qualifiedName
- [smithery-list-skills-example.json](examples/smithery-list-skills-example.json) — Search the skills directory
- [smithery-create-connection-example.json](examples/smithery-create-connection-example.json) — Create a Connect API connection
- [smithery-create-service-token-example.json](examples/smithery-create-service-token-example.json) — Issue a scoped service token
- [smithery-mcp-endpoint-example.json](examples/smithery-mcp-endpoint-example.json) — POST a JSON-RPC tools/call through the Connect MCP endpoint
- [smithery-list-triggers-example.json](examples/smithery-list-triggers-example.json) — List triggers on a connection

### Vocabulary
- [smithery-vocabulary.yml](vocabulary/smithery-vocabulary.yml) — MCP, registry, Connect, and Smithery platform vocabulary

### Commercial Surface
- [smithery-plans-pricing.yml](plans/smithery-plans-pricing.yml) — Plans scaffold (API Commons Plans 0.1)
- [smithery-rate-limits.yml](rate-limits/smithery-rate-limits.yml) — Rate limits scaffold (API Commons Rate Limits 0.1)
- [smithery-finops.yml](finops/smithery-finops.yml) — FinOps Framework / FOCUS 1.3 alignment

## Authentication

- **Bearer Token (API Key)** — `Authorization: Bearer <key>` using a key from `smithery.ai/account/api-keys`. Long-lived; backend use.
- **Service Token** — Scoped, time-limited tokens issued via `POST /tokens` for browser/mobile/agent contexts. Used by the Connect MCP endpoint.
- **OAuth 2.0 (Upstream)** — Smithery manages the OAuth handshake with upstream providers on the user's behalf when a connection is created, handling client registration via Client ID Metadata Documents.

## Connect Gateway

The Connect API exposes a single MCP endpoint per namespace:

```
https://mcp.smithery.run/{namespace}
```

Or per-connection through the Platform API:

```
POST https://api.smithery.ai/connect/{namespace}/{connectionId}/mcp
```

This is a streamable-HTTP JSON-RPC transport that proxies agent calls to the underlying MCP server bound to the connection.

## Developer Resources

- [Documentation](https://smithery.ai/docs)
- [API Reference](https://smithery.ai/docs/api-reference)
- [CLI Docs](https://smithery.ai/docs/concepts/cli) — `npm install -g smithery@latest` (Node.js 20+)
- [GitHub Organization](https://github.com/smithery-ai) — 36 public repos
- [TypeScript SDK (@smithery/api)](https://github.com/smithery-ai/typescript-api) — Stainless-generated
- [Smithery Cookbook](https://github.com/smithery-ai/smithery-cookbook) — Recipes
- [Playground](https://smithery.ai/playground)
- [Blog](https://smithery.ai/blog)
- [OpenAPI JSON](https://smithery.ai/docs/openapi.json)
- [llms.txt](https://smithery.ai/docs/llms.txt)
