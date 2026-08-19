# Instalação detalhada

Tribunal TSE: Situação Eleitoral é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_tribunal_tse_situacao`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_tribunal_tse_situacao` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_tribunal_tse_situacao` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_tribunal_tse_situacao` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.tribunal_tse_situacao` (ou `servers.tribunal_tse_situacao` no VS Code) do config do cliente e reinicie.
