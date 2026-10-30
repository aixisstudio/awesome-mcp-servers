# Awesome Mcp Servers

[English](README.md) | **Français** | [Español](README.es.md) | [中文](README.zh-CN.md) | [日本語](README.ja.md) | [Русский](README.ru.md)

Serveurs MCP — l'annuaire des outils Model Context Protocol

Qu'est-ce que le MCP ?

**Modèle Context Protocol** (Anthropique, standard ouvert) – l'outil USB-C de l'IA : un protocole qui permet à tout client LLM de parler à n'importe quelle source d'outils/données. Un serveur MCP expose **outils**, **ressources** et **prompts**; le client (Claude Desktop, Cursor, votre agent) les appelle.

Répertoire du serveur

Données et bases de données
Serveur Qu'est-ce qu'il connecte
|---|---|
`postgres`?Répondre + inspecter PostgreSQL?
Accès SQLite local
`redis`: Valeur clé ops
Questions analytiques
Recherches d'entrepôt

Web et navigation
Serveur Qu'est-ce qu'il connecte
|---|---|
Contrôle complet du navigateur
`puppeteer`= Navigateur sans tête
Demandes HTTP
Recherche Web
`firecrawl`-Scrate → marqueur propre

Fichiers et système
Serveur Qu'est-ce qu'il connecte
|---|---|
`filesystem`=Accès au fichier étendu
Opérations de pension
`shell`=Exécution de commande (précieuse!)
Gestion des conteneurs

Plateformes Dev
Serveur Qu'est-ce qu'il connecte
|---|---|
Questions, relations publiques, repos
Même chose pour GitLab
`linear`?Suivi des problèmes
`sentry`: Surveillance des erreurs
Ressources en nuage

Productivité
Serveur Qu'est-ce qu'il connecte
|---|---|
Messages, canaux
Docs et bases de données
Fichiers `google-drive`
Événements
Tâches

Mémoire et connaissance
Serveur Qu'est-ce qu'il connecte
|---|---|
`memory`
Recherche vectorielle
`chroma`-Store local d'intégration

Écrire vos propres (10 lignes)

```python
# python-sdk example
from mcp.server.fastmcp import FastMCP
mcp = FastMCP("my-server")

@mcp.tool()
def hello(name: str) -> str:
    return f"Hello {name}"

mcp.run()
```

S'inscrire dans Claude Desktop : `claude_desktop_config.json` → `mcpServers`.

Note de sécurité

- Les serveurs MCP fonctionnent **code local** — audit avant installation
- Préférer l'accès au système de fichiers scoped sur `/`
- Les descriptions d'outils sont injectables — traiter la sortie du serveur comme non fiable

---
## Contribuer

Les pull requests sont les bienvenues : ouvre une PR, elle sera relue et fusionnée. Maintenu par [aixisstudio](https://github.com/aixisstudio), auteur de [Snitch](https://github.com/aixisstudio/Snitch), pare-feu applicatif open source.

## Licence: MIT
