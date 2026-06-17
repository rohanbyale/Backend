# Awesome MCP Servers

A curated, categorized list of Model Context Protocol (MCP) servers — useful for developers, coders, and AI-assisted workflows.

> MCP (Model Context Protocol) is an open standard that lets AI assistants connect to external tools and data sources through standardized "servers." Each server below adds a specific capability — file access, database queries, GitHub management, browser automation, and more.

## Contents

- [Official / Reference Servers](#official--reference-servers)
- [File Systems & Local Tools](#file-systems--local-tools)
- [Version Control](#version-control)
- [Databases](#databases)
- [Cloud Platforms & DevOps](#cloud-platforms--devops)
- [Browser & Web Automation](#browser--web-automation)
- [Communication & Productivity](#communication--productivity)
- [Search & Knowledge](#search--knowledge)
- [Monitoring & Observability](#monitoring--observability)
- [Security](#security)
- [Curated Lists Used as Sources](#curated-lists-used-as-sources)
- [How to Use These Servers](#how-to-use-these-servers)
- [Contributing](#contributing)

---

## Official / Reference Servers
Maintained by the MCP steering group as canonical examples.

| Server | Description |
|---|---|
| [Filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) | Secure, scoped read/write file operations on local directories |
| [Git](https://github.com/modelcontextprotocol/servers/tree/main/src/git) | Read, search, and manipulate local Git repositories |
| [Fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) | Fetches and converts web content for LLM consumption |
| [Memory](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) | Knowledge-graph based persistent memory across sessions |
| [Sequential Thinking](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking) | Structured, step-by-step reasoning for complex problems |
| [Time](https://github.com/modelcontextprotocol/servers/tree/main/src/time) | Time zone lookups and conversions |

## File Systems & Local Tools
| Server | Description |
|---|---|
| Filesystem (community variants) | Extended versions of the official filesystem server with extra permission controls |
| Backup | File/folder backup and restore for agent workflows |
| eBook-mcp | Lets an LLM read and query local PDF/EPUB ebooks |

## Version Control
| Server | Description |
|---|---|
| [github-mcp-server](https://github.com/github/github-mcp-server) | Official GitHub integration — repos, PRs, issues, code search |
| GitLab MCP | Project, issue, and CI/CD pipeline management on GitLab |
| Gitea MCP | Interact with self-hosted Gitea instances |
| mcp-git-ingest | Summarizes and analyzes GitHub repos in a prompt-friendly way |
| Octocode | AI-assisted code research and discovery across large GitHub ecosystems |

## Databases
| Server | Description |
|---|---|
| PostgreSQL | Query and inspect Postgres schemas with read/write controls |
| MySQL | Configurable-access MySQL integration with schema inspection |
| SQLite | Local SQLite querying with built-in analysis tools |
| MongoDB | Query and analyze MongoDB collections |
| BigQuery | Schema exploration and read-only SQL queries on BigQuery |
| Snowflake | Read/write Snowflake integration with insight tracking |
| Airtable | Read/write access to Airtable bases with schema inspection |

## Cloud Platforms & DevOps
| Server | Description |
|---|---|
| AWS CDK | Prescriptive AWS CDK advice, Nag-rule checks, pattern discovery |
| Google Cloud Run | Deploy directly to Cloud Run |
| Cloudflare | Manage Workers, KV, R2, and D1 |
| Azure DevOps (multiple implementations) | Work items, pipelines, repo management on Azure DevOps |
| Alibaba Cloud Ops | Manage ECS, Cloud Monitor, and OOS resources |
| Docker | Container and compose-stack management |
| Kubernetes | Cluster operations through MCP |
| Metoro | Query Kubernetes environments monitored by Metoro |

## Browser & Web Automation
| Server | Description |
|---|---|
| Puppeteer | Browser automation for scraping and interaction |
| Fetch | Lightweight page fetching and content conversion |
| Oxylabs | Web scraping with dynamic rendering support |
| GoLogin | Automate and manage browser profiles |

## Communication & Productivity
| Server | Description |
|---|---|
| Slack | Channel and message management |
| Notion (multiple implementations) | Manage notes and todo lists via the Notion API |
| Linear | Issue tracking integration |
| Todoist | Natural-language task management |
| Atlassian | Jira + Confluence integration |
| Dart | Task, doc, and project data for AI-native project management |

## Search & Knowledge
| Server | Description |
|---|---|
| Brave Search | Web search via Brave's Search API |
| Qdrant | Vector search for storing/retrieving AI memories |
| LlamaCloud | Connects to a managed LlamaCloud index |
| HuggingFace Spaces | Use HF Spaces (image/audio/text models) as tools |

## Monitoring & Observability
| Server | Description |
|---|---|
| Sentry | Error tracking and performance monitoring |
| Raygun | Crash reporting and real-user monitoring |
| Dash0 | OpenTelemetry resource navigation and incident investigation |
| Grafana | Search dashboards and query datasources |

## Security
| Server | Description |
|---|---|
| Cycode | SAST, SCA, secrets, and IaC scanning in the dev lifecycle |
| GhidraMCP | Binary analysis and reverse engineering via Ghidra |
| Shodan MCP | IP lookups, device search, and CVE queries via Shodan |
| Bitwarden/Vaultwarden MCP | Manage vault items (logins, notes, SSH keys) via the official CLI |

---

## Curated Lists Used as Sources
These are larger "awesome lists" worth browsing directly for the full long-tail of servers:

- https://github.com/modelcontextprotocol/servers — official reference repo
- https://github.com/punkpeye/awesome-mcp-servers — largest general community list
- https://github.com/wong2/awesome-mcp-servers — another large, actively updated list
- https://github.com/rohitg00/awesome-devops-mcp-servers — DevOps-specific list
- https://github.com/appcypher/awesome-mcp-servers — categorized general list

## How to Use These Servers
Most servers run locally via `npx` (Node) or `uvx`/`pip` (Python), and are registered in your MCP client's config.

Example `claude_desktop_config.json` entry:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/folder"]
    }
  }
}
```

Check each server's own README for its exact install command and required environment variables (API keys, tokens).

**Security note:** only install servers from sources you trust — they can run with the same permissions as your AI client. Scope filesystem/database access narrowly and keep credentials in environment variables.

## Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add a server to this list.

## License
[MIT](LICENSE)
