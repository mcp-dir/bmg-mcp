# Instalação rápida

Conector MCP.AI para Banco BMG é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_bmg`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Conector MCP.AI para Banco BMG` / `https://api.mcp.ai/p_bmg`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "bmg": { "type": "http", "url": "https://api.mcp.ai/p_bmg" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=bmg&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9ibWcifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "bmg": { "url": "https://api.mcp.ai/p_bmg" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=bmg&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_bmg%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "bmg": { "type": "http", "url": "https://api.mcp.ai/p_bmg" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_bmg
```

Dúvidas? [bmg@mcp.ai](mailto:bmg@mcp.ai)
