# Mapa de integrações

Este documento descreve como verificar integrações sem presumir que a disponibilidade de uma ferramenta equivale a acesso ao projeto.

| Integração | Verificação necessária | Evidência mínima | Estado deste projeto |
|---|---|---|---|
| GitHub | Repositório, identidade da conexão, escopos e permissão efetiva | Consulta de leitura ao repositório e registro do escopo | Verificar por sessão e repositório |
| Linear | Workspace, equipes, projetos e issues relevantes | Consultas de leitura separadas | Verificar por workspace e equipe |
| Manus Studio | Sessão e workspace selecionado | Tela atual e acesso ao projeto | Verificar no workspace em uso |
| CUE / Cue.im | Sessão CUE e recursos conectados | Sessão autenticada e evidência direta do recurso | Verificar separadamente de Manus Studio |
| Google OAuth | Configuração, consentimento, emissão de token e chamada autenticada | Evidência independente para cada etapa | Documentação estática não comprova autenticação |

## Regras

- Registre cada produto e conexão separadamente; conectores do mesmo fornecedor não são equivalentes.
- Use somente leitura para verificar estado. Não faça login, aceite escopos ou altere conexão sem solicitação específica.
- Nunca registre valores de tokens, cookies, chaves ou client secrets.
- `unknown` significa que não houve evidência suficiente; não significa que a integração inexiste.
