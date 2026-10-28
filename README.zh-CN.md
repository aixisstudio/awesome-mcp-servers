# Awesome Mcp Servers

[English](README.md) | [Français](README.fr.md) | [Español](README.es.md) | **中文** | [日本語](README.ja.md) | [Русский](README.ru.md)

MCP 服务器目录

_详细内容（列表、链接、描述）以英文维护 — 以下章节为你指引。_

## 🔌 What is MCP?

**Model Context Protocol** (Anthropic, open standard) — the USB-C of AI tooling: one protocol that lets any LLM client talk to any tool/data source. A MCP server exposes **tools**, **resources**, and **prompts**; the client (Claude Desktop, Cursor, your agent) calls them.

## 📂 Server directory

### 🗄️ Data & Databases
| Server | What it connects |
|---|---|
| `postgres` | Query + inspect PostgreSQL |
| `sqlite` | Local SQLite access |
| `redis` | Key-value ops |
| `clickhouse` | Analytics queries |
| `snowflake` | Warehouse queries |

### 🌐 Web & Browsing
| Server | What it connects |
|---|---|
| `playwright` | Full browser control |
| `puppeteer` | Headless browser |
| `fetch` | HTTP requests |
| `brave-search` | Web search |
| `firecrawl` | Scrape → clean markdown |

### 🗂️ Files & System
| Server | What it connects |
|---|---|
| `filesystem` | Scoped file access |
| `git` | Repo operations |
| `shell` | Command execution (careful!) |
| `docker` | Container management |

### 🧰 Dev Platforms
| Server | What it connects |
|---|---|
| `github` | Issues, PRs, repos |
| `gitlab` | Same for GitLab |
| `linear` | Issue tracking |
| `sentry` | Error monitoring |
| `aws` | Cloud resources |

### 📅 Productivity
| Server | What it connects |
|---|---|
| `slack` | Messages, channels |
| `notion` | Docs & databases |
| `google-drive` | Files |
| `google-calendar` | Events |
| `todoist` | Tasks |

### 🧠 Memory & Knowledge
| Server | What it connects |
|---|---|
| `memory` | Persistent knowledge graph |
| `qdrant` | Vector search |
| `chroma` | Local embeddings store |

## 🛠️ Write your own (10 lines)

```python
# python-sdk example
from mcp.server.fastmcp import FastMCP
mcp = FastMCP("my-server")

@mcp.tool()
def hello(name: str) -> str:
    return f"Hello {name}"

mcp.run()
```

Register in Claude Desktop: `claude_desktop_config.json` → `mcpServers`.

## 🔐 Security notes

- MCP servers run **local code** — audit before installing
- Prefer scoped filesystem access over `/`
- Tool descriptions are prompt-injectable — treat server output as untrusted

---
## 贡献

欢迎提交 Pull Request，我们会审查并合并。由 [aixisstudio](https://github.com/aixisstudio) 维护，他也是开源应用防火墙 [Snitch](https://github.com/aixisstudio/Snitch) 的作者。

## 许可证: MIT
