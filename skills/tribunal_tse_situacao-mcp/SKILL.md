---
name: tribunal_tse_situacao-mcp
description: Skill da REST API do Tribunal TSE: Situação Eleitoral na MCP.AI: 1 endpoint em /api/tribunal_tse_situacao. Tribunal TSE: Situação Eleitoral, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TSE: Situação Eleitoral — REST API skill

Você tem acesso à **Tribunal TSE: Situação Eleitoral** REST API na MCP.AI.

> Tribunal TSE: Situação Eleitoral, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tse_situacao
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/tribunal_tse_situacao/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tse_situacao/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tse_situacao_consultar`

Tribunal TSE: Situação Eleitoral, consulta em fonte oficial. _(POST /api/tribunal_tse_situacao/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `name` | string | Não | Parâmetro de consulta "name". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `titulo_eleitoral` | string | Não | Parâmetro de consulta "titulo_eleitoral". |
| `birthdate` | string | Não | Parâmetro de consulta "birthdate". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tse_situacao` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
