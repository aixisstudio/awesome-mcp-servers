# Awesome Mcp Servers

[English](README.md) | [Français](README.fr.md) | [Español](README.es.md) | [中文](README.zh-CN.md) | **日本語** | [Русский](README.ru.md)

MCP サーバー一覧

##  What MCPとは?

**Model Context Protocol** (Anthropic, Open Standard) — AI ツーリングの USB-C: LLM クライアントが任意のツール/データソースに話せるプロトコル。 MCP サーバーは、**tools**、**resources**、**prompts**を明示します。クライアント(デスクトップ、カーソル、エージェント)はそれらを呼び出す。

## クライアントディレクトリ

## ️️ データとデータベース
| サーバー | 接続について |
|---|---|
| `postgres` | お問い合わせ | PostgreSQL の検査 |
| `sqlite` | ローカルSQLiteアクセス |
| `redis` | キーバリューオプス |
| `clickhouse` | 解析クエリ |
| `snowflake` | 倉庫問い合わせ |

#### インポート ウェブ & ブラウジング
| サーバー | 接続について |
|---|---|
| `playwright` | フルブラウザコントロール |
| `puppeteer` | ヘッドレスブラウザ |
| `fetch` | HTTPリクエスト |
| `brave-search` | ウェブ検索 |
| `firecrawl` | スクラップ → クリーンマークダウン |

#### は、ファイルとシステム
| サーバー | 接続について |
|---|---|
| `filesystem` | サイトマップ |
| `git` | リポ操作 |
| `shell` | コマンド実行 |
| `docker` | コンテナ管理 |

### 開発者プラットフォーム
| サーバー | 接続について |
|---|---|
| `github` | 課題・広報・リポーズ |
| `gitlab` | GitLabと同じ |
| `linear` | 課題追跡 |
| `sentry` | エラーモニタリング |
| `aws` | クラウドリソース |

##### 加工精度
| サーバー | 接続について |
|---|---|
| `slack` | メッセージ・チャンネル |
| `notion` | ドキュメント・データベース |
| `google-drive` | ファイル |
| `google-calendar` | イベント |
| `todoist` | タスク |

### 🧠 記憶と知識
| サーバー | 接続について |
|---|---|
| `memory` | 永続的知識グラフ |
| `qdrant` | ベクトル検索 |
| `chroma` | 地域密着店舗 |

## ️️ 自分で書いて (10 行)

```python
# python-sdk example
from mcp.server.fastmcp import FastMCP
mcp = FastMCP("my-server")

@mcp.tool()
def hello(name: str) -> str:
    return f"Hello {name}"

mcp.run()
```

Claudeデスクトップに登録: `claude_desktop_config.json` → `mcpServers`.

## 🔐 セキュリティノート

- MCP サーバーが実行**ローカル コード** — インストール前に監査
- `/` 上での優先スコープ付きファイルシステムアクセス
- ツールの説明はプロンプト注射可能 — 信頼できないようにサーバーの出力を扱います

---
## 貢献

プルリクエストを歓迎します。レビューしてマージします。[aixisstudio](https://github.com/aixisstudio) による管理 — オープンソースのアプリケーションファイアウォール [Snitch](https://github.com/aixisstudio/Snitch) の作者です。

## ライセンス: MIT
