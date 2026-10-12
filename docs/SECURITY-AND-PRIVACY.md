# Segurança, identidade e privacidade

## Classificação de dados

- **Público:** prompts genéricos, documentação de uso, templates vazios, relatórios sanitizados.
- **Interno:** inventários detalhados, nomes de ambientes, diferenças de repositórios e resultados operacionais não sensíveis.
- **Confidencial:** tokens, client secrets, cookies, chaves privadas, arquivos `.env`, dados pessoais não necessários, URLs privadas com credenciais e dados de autenticação.
- **Restrito:** material cuja divulgação possa comprometer contas, sistemas ou terceiros; acesso mínimo e registro de autorização.

## Regras obrigatórias

1. Nunca incluir segredos em Markdown, issues, commits, logs ou saídas do agente.
2. Redigir valores sensíveis; quando necessário, registrar apenas presença, tipo, escopo, localização lógica e resultado da verificação.
3. Não pedir ao usuário que cole tokens ou segredos no chat.
4. Usar autenticação já autorizada pelo provedor; não tentar contornar MFA, OAuth, permissões ou políticas do Manus.
5. Não tratar a permissão ADMIN no GitHub como autorização automática para qualquer ação.
6. Não publicar dados de conta, e-mail privado, identificadores pessoais ou caminhos locais desnecessários.
7. Separar a identidade pública de contribuição da identidade legal quando isso for relevante.
8. Proteger o repositório privado com menor privilégio, revisão de colaboradores e verificação de visibilidade.
9. Se houver suspeita de vazamento, interromper a publicação, registrar evidência sanitizada e solicitar decisão do responsável sobre contenção/rotação.
10. Não prometer anonimato absoluto: metadados de GitHub, commits e serviços externos podem revelar informações de conta.

## Registro de auditoria

Cada ação deve incluir:
- ID e horário da tarefa, com fuso horário;
- agente e ambiente que a executaram;
- objetivo e autorização correspondente;
- modo `READ_ONLY`, `PROPOSE` ou `WRITE_APPROVED`;
- caminhos/recursos afetados;
- resultado e limitações;
- hash ou commit quando aplicável;
- estado final e responsável pela aprovação.

## Publicação segura

Antes de cada commit público, verificar `.env`, arquivos de credenciais, dumps, logs, caminhos pessoais, nomes de clientes, dados privados e histórico de Git. Um scanner sem ocorrências não é prova de ausência absoluta de segredos.
