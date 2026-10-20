# NODE249 Assurance · Plugins para agentes de IA

Conecta tu agente de IA a los **manuales de buenas prácticas de desarrollo de NODE249 Assurance** para que, al
programar en cualquier lenguaje o tecnología, consulte el manual correspondiente y pase su lista de comprobación antes
de dar el trabajo por terminado.

Los manuales se sirven desde el servidor MCP `https://assurance.node249.com/mcp` y **requieren una cuenta de NODE249
Assurance** (solo por invitación: hola@node249.com). Este repositorio solo contiene la configuración y las
instrucciones para el agente: ningún manual, token ni secreto.

## 1. Crea tu token
En https://assurance.node249.com/app/seguridad › **Tokens de API**. Es personal, de solo lectura y caduca. Guárdalo en
la variable de entorno `NODE249_ASSURANCE_TOKEN` (nunca en un repositorio).

## 2. Claude Code
```text
/plugin marketplace add node249-com/assurance-plugins
/plugin install node249-assurance@node249
```
El plugin añade el servidor MCP (lee el token de `NODE249_ASSURANCE_TOKEN`) y la skill `buenas-practicas-node249`, que
indica a Claude cuándo consultar los manuales. No ejecuta código en tu equipo ni envía tu código al servidor.

Sin plugin, solo la conexión:
```bash
claude mcp add --transport http --scope user node249-assurance https://assurance.node249.com/mcp --header "Authorization: Bearer $NODE249_ASSURANCE_TOKEN"
```

## 3. Codex
- Añade [`codex/config.toml`](codex/config.toml) a `~/.codex/config.toml`.
- Copia el bloque [`codex/AGENTS.md`](codex/AGENTS.md) en el `AGENTS.md` de tu proyecto.

## 4. Otros clientes MCP (Cursor…)
```json
{ "mcpServers": { "node249-assurance": { "url": "https://assurance.node249.com/mcp", "headers": { "Authorization": "Bearer <tu token>" } } } }
```

## Herramientas (solo lectura)
`listar_manuales` · `leer` (procedimiento o capítulo del libro) · `buscar` · `lista_comprobacion`

---
© NODE 249. Todos los derechos reservados.
