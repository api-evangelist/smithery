# Smithery

Smithery is a platform for discovering, deploying, and managing Model Context Protocol (MCP) servers and skills. It provides a registry of 6000+ community-built MCP extensions that AI agents can use to access external tools, data sources, and services. The platform offers APIs for server management, skill discovery, connection management, and AI-agent integration.

## APIs

| API | Description |
|-----|-------------|
| [Registry API](openapi/smithery-openapi.json) | MCP server registry, skills, connections, namespaces, tokens |

## Artifacts

### OpenAPI Specifications
- [smithery-openapi.json](openapi/smithery-openapi.json) — Full Registry API specification (official Smithery OpenAPI)

### Capabilities
- [mcp-server-discovery.yaml](capabilities/mcp-server-discovery.yaml) — MCP server and skill discovery workflow

#### Shared Definitions
- [capabilities/shared/registry-api.yaml](capabilities/shared/registry-api.yaml) — Registry API capability definition

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

### Vocabulary
- [smithery-vocabulary.yml](vocabulary/smithery-vocabulary.yml) — MCP and Smithery platform vocabulary

## Authentication

- **Bearer Token** — API keys from smithery.ai/account/api-keys used as Bearer tokens
- **OAuth 2.0** — Supported for client authorization flows

## Developer Resources

- [Documentation](https://smithery.ai/docs)
- [CLI](https://smithery.ai/docs/concepts/cli)
- [GitHub Organization](https://github.com/smithery-ai)
- [Playground](https://smithery.ai/playground)
- [Blog](https://smithery.ai/blog)
- [OpenAPI Spec](https://smithery.ai/docs/openapi.json)
