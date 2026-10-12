# Checklist de segurança

## Antes de editar ou publicar

- [ ] Confirmar o escopo, a fonte e a autorização para cada mudança.
- [ ] Verificar `git status`, branch e diff completos.
- [ ] Excluir `.env`, credenciais, dumps, logs, dados pessoais e metadados locais.
- [ ] Revisar origem, licença e atribuição de conteúdo de terceiros.
- [ ] Distinguir resultado de scanner de garantia de ausência de segredos.
- [ ] Confirmar visibilidade e público destinatário.
- [ ] Preparar rollback e evidência verificável.
- [ ] Obter aprovação específica antes de commit, push, merge, deploy ou alteração de permissão.

## Após a verificação

Registre os arquivos examinados, padrões usados, resultado, limitações, data e ambiente. Não reproduza valores detectados. Se houver possível segredo ou dúvida de titularidade, interrompa a publicação e peça decisão humana.
