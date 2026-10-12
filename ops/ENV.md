# Variáveis de ambiente

O arquivo `.env.example` documenta nomes de variáveis; ele não contém credenciais funcionais. Valores devem permanecer no ambiente seguro que executa cada ferramenta.

| Grupo | Nomes declarados |
|---|---|
| Manus runtime | `MANUS_API_KEY` |
| GitHub CLI / Git HTTPS | `GH_TOKEN`, `COPILOT_GITHUB_TOKEN`, `GITHUB_TOKEN` |
| Copilot cloud agent MCP | `COPILOT_MCP_GITHUB_PERSONAL_ACCESS_TOKEN` |
| Provedores de IA | `OPENAI_API_KEY`, `GEMINI_API_KEY`, `GOOGLE_API_KEY` |

## Cuidados

- Não copie valores para Markdown, prompts, logs, issues ou commits.
- Não confunda a credencial do runtime Manus com OAuth do GitHub ou com um conector de produto.
- Não carregue secrets de produção em ferramentas de desenvolvimento.
- A presença do nome de uma variável não comprova que exista um valor, que ele seja válido ou que uma conexão esteja autenticada.
