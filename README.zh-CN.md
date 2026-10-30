# Awesome Mcp Servers

[English](README.md) | [Français](README.fr.md) | [Español](README.es.md) | **中文** | [日本語](README.ja.md) | [Русский](README.ru.md)

MCP 服务器目录

□□□□□□□□□何为MCP?

** 模式上下文协议**(Anthropic,开放标准)——AI工具的USB-C:一个让任何LLM客户端与任何工具/数据源交谈的协议. MCP服务器会曝光**tools**,**资源**,**瞬间**;客户端(Claude Desktop,cursor,你的代理商)会调用它们.

# # # #% 服务器目录

数据数据库
# # 服务器 # # 它连接 # # # #
|---|---|
`postgres` 查询+检查 PostgreSQL
`sqlite` 本地 SQLite 访问
`redis` 键值操作
`clickhouse` 分析查询
`snowflake` 仓库查询

QQ 网络浏览
# # 服务器 # # 它连接 # # # #
|---|---|
QQ `playwright` QQ 完整浏览器控制QQ
`puppeteer` 无头浏览器 QQ
`fetch` HTTP请求 QQ
`brave-search`网络搜索
~ `firecrawl` ~ 擦干净的标记~

QQ 文件与系统
# # 服务器 # # 它连接 # # # #
|---|---|
`filesystem` 范围文件访问
`git` 回波操作
`shell` 命令执行(小心!)
`docker` 集装箱管理

* * * * * * *
# # 服务器 # # 它连接 # # # #
|---|---|
`github` 问题、公关、重置
GitLab的`gitlab`也一样。
`linear` 问题追踪
`sentry` 错误监测
`aws` 云资源

生产率
# # 服务器 # # 它连接 # # # #
|---|---|
`slack` 信件、频道
`notion` 文档和数据库
`google-drive` 文件 # # # #
`google-calendar` 活动
`todoist` 任务

QQ 记忆和知识
# # 服务器 # # 它连接 # # # #
|---|---|
`memory` 持久知识图
`qdrant` 矢量搜索
`chroma` 本地嵌入存储器

□ □ □ 写你自己( 10行)

```python
# python-sdk example
from mcp.server.fastmcp import FastMCP
mcp = FastMCP("my-server")

@mcp.tool()
def hello(name: str) -> str:
    return f"Hello {name}"

mcp.run()
```

在克劳德桌面注册: `claude_desktop_config.json` → `mcpServers`.

□ 安全说明

- MCP服务器运行**本地代码**——在安装前进行审计
- 在`/`上优先访问范围文件系统
- 工具描述是可迅速注入的——将服务器输出视为不信任

---
## 贡献

欢迎提交 Pull Request，我们会审查并合并。由 [aixisstudio](https://github.com/aixisstudio) 维护，他也是开源应用防火墙 [Snitch](https://github.com/aixisstudio/Snitch) 的作者。

## 许可证: MIT
