# L4 — MCP como Integraciones (Model Context Protocol)

## La analogía

| No-Code | Claude Code + MCP |
|---|---|
| Conector de Make / integración de n8n | MCP Server |
| API key en la integración | Configuración en `mcp_servers` |
| Trigger "cuando llega un dato de X" | Claude consulta MCP en tiempo real |
| Output de un módulo externo | Datos que Claude recibe del MCP |

MCP permite que Claude acceda a herramientas y datos externos directamente durante la conversación — sin copiar/pegar, sin salir del contexto.

## Casos de uso reales para tu stack

| Herramienta | Lo que habilita MCP |
|---|---|
| Google Drive / Docs | Claude lee y escribe documentos directamente |
| Airtable | Claude consulta y actualiza registros |
| GitHub | Claude lee código, PRs, issues sin salir del chat |
| HubSpot / Zoho | Claude consulta deals, contactos, actividad |
| Notion | Claude lee/escribe páginas y bases de datos |
| Slack | Claude envía mensajes o lee canales |

## Cómo configurar un MCP Server

En `~/.claude/settings.json` (o en el proyecto):

```json
{
  "mcpServers": {
    "google-drive": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-server-gdrive"]
    },
    "airtable": {
      "command": "npx",
      "args": ["-y", "mcp-server-airtable"],
      "env": {
        "AIRTABLE_API_KEY": "tu-api-key"
      }
    }
  }
}
```

## Dónde encontrar MCP Servers

- **Oficial Anthropic:** github.com/anthropics/mcp-servers
- **Directorio comunitario:** mcp.so
- **npm:** busca `mcp-server-[herramienta]`

## Ejercicio de primera semana

Conecta Claude a Google Drive (el MCP más sencillo). Luego pídele que lea un documento y lo analice. Ese flujo que antes requería copiar/pegar ahora es una instrucción directa.

## Siguiente nivel

Una vez que tienes 2-3 MCPs activos, puedes hacer cosas como:
- "Revisa los últimos 5 deals de HubSpot y dame un resumen ejecutivo"
- "Busca en Airtable los proyectos activos y crea un plan de acción"
- "Lee el brief en Google Drive y genera el copy para el email"

Esto es operar Claude como un copilot operacional real, no como un chatbot de texto.
