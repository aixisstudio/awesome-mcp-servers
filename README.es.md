# Awesome Mcp Servers

[English](README.md) | [Français](README.fr.md) | **Español** | [中文](README.zh-CN.md) | [日本語](README.ja.md) | [Русский](README.ru.md)

Servidores MCP — directorio de herramientas

## 🔌 ¿Qué es MCP?

**Model Context Protocol** (Antropo, estándar abierto) — el USB-C de la herramienta AI: un protocolo que permite a cualquier cliente LLM hablar con cualquier fuente de herramientas/datos. Un servidor MCP expone **herramientas**, **resources**, y **prompts**; el cliente (Claude Desktop, Cursor, su agente) los llama.

## 📂 Directorio del servidor

Datos sobre bases de datos
← Servidor Silencio Lo que conecta
|---|---|
Silencio `postgres` Silencio Query + inspeccionar PostgreSQL
Silencio `sqlite` Silencio acceso local de SQLite
Silencio `redis`
Silencio `clickhouse`
Silencio `snowflake`

### 🌐 Web &amp; Browsing
← Servidor Silencio Lo que conecta
|---|---|
Silencio `playwright` Silencio Control completo del navegador Silencio
Silencio `puppeteer`
TEN TERRITOR SON TEN SON SON ANTERIOR
Silencio `brave-search` Silencio Búsqueda web
Silencio `firecrawl` Silencioso → marcación limpia

#### 🗂ف Files &amp; System
← Servidor Silencio Lo que conecta
|---|---|
Silencio `filesystem` Silencio Acceso a archivos escocidos
Silencio `git`
Silencio `shell` ¦ Ejecución del comando (cuidado!)
Silencio `docker`

### 🧰 Dev Platforms
← Servidor Silencio Lo que conecta
|---|---|
← `github` ← Problemas, PRs, repos
TENIDO `gitlab` TENIDO Lo mismo para GitLab
Silencio `linear`
Silencio `sentry`
confidencialidad `aws`

#### 📅 Productivity
← Servidor Silencio Lo que conecta
|---|---|
Silencio `slack` Silencio Mensajes, canales
Silencio `notion` Silencio Docs &amp; bases de datos
Silencio `google-drive` Silenciosos archivos
confidencialidad `google-calendar`
confidencialidad `todoist` Silencioso

#### 🧠 Memoria &gt; Conocimiento
← Servidor Silencio Lo que conecta
|---|---|
Silencio `memory`
Silencio `qdrant`
Silencio `chroma`

## 🛠Cambia tus propias (10 líneas)

```python
# python-sdk example
from mcp.server.fastmcp import FastMCP
mcp = FastMCP("my-server")

@mcp.tool()
def hello(name: str) -> str:
    return f"Hello {name}"

mcp.run()
```

Regístrate en Claude Desktop: `claude_desktop_config.json` → `mcpServers`.

Notas de seguridad

- Los servidores MCP ejecutan **código local** — auditoría antes de instalar
- Preferencia acceso a los sistemas de archivos de alcance superior a `/`
- Las descripciones de las herramientas son inyectables rápidamente — tratar la salida del servidor como no confiable

---
## Contribuir

Los pull requests son bienvenidos: abre una PR y será revisada y fusionada. Mantenido por [aixisstudio](https://github.com/aixisstudio), autor de [Snitch](https://github.com/aixisstudio/Snitch), firewall de aplicaciones open source.

## Licencia: MIT
