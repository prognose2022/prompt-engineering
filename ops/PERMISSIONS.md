# Matriz de permissões

Permissão técnica não é autorização para executar qualquer ação. A autoridade humana mantém a decisão final sobre identidade, licença, publicação e produção.

| Ator / integração | Leitura | Escrita local | Escrita remota | Publicação / produção |
|---|---|---|---|---|
| Responsável humano | Conforme conta e recurso | Conforme decisão | Conforme autorização explícita | Aprovação explícita necessária |
| Agente nesta tarefa | Somente fontes observadas | Somente escopo autorizado | Requer autorização específica | Requer autorização específica |
| GitHub connector | Confirmar por repositório | Não aplicável | Requer autorização específica | Requer autorização específica |
| Linear connector | Confirmar por workspace | Não aplicável | Requer autorização específica | Não aplicável |
| Manus Studio / CUE | Confirmar no workspace ativo | Conforme escopo autorizado | Requer autorização específica | Requer autorização específica |

## Regras de menor privilégio

1. Verifique identidade e recurso antes de cada operação.
2. Separe planejamento, edição, commit, push, merge e deploy.
3. Exija autorização específica antes de alterar credenciais, permissões, configurações, branches, issues ou dados de produção.
4. Não deduza autorização de escrita a partir de uma resposta `admin` da API.
5. Registre o resultado e a evidência sem expor dados sensíveis.
