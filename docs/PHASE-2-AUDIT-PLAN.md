# Fase 2 — Plano de auditoria controlada

## Objetivo

Preparar o projeto `prompt-engineering` para produção gradual, preservando a identidade do responsável, a integridade do snapshot-base e a confidencialidade de credenciais, projetos privados e dados pessoais.

## Fases de execução

### 2.1 — Identidade do agente e escopo de acesso
- Registrar que o executor é o multiagente CUE no Manus Studio; não confundir com um executável local chamado `cue`.
- Registrar identificador da tarefa, ambiente, conectores disponíveis e limitações.
- Distinguir: autoridade administrativa humana, agente que planeja, agente que executa, revisor e publicador.
- Não inferir acesso ao Mac a partir de acesso à sandbox.
- Não solicitar nem imprimir tokens, segredos, cookies, chaves privadas ou conteúdo de arquivos de credenciais.

### 2.2 — Integridade e proveniência
- Inventariar arquivos e registrar caminho relativo, tamanho, SHA-256, origem e classificação de confidencialidade.
- Registrar os ZIPs originais e seus hashes, sem alterá-los.
- Comparar projeto local, artefatos ZIP e GitHub somente quando cada fonte estiver acessível.
- Tratar divergências como itens de análise; nunca resolver por sobrescrita automática.

### 2.3 — Segurança e autenticação
- Fazer inspeção somente de leitura das configurações disponíveis.
- Registrar presença, escopos declarados e estado observável do OAuth sem revelar segredos.
- Distinguir configuração estática, consentimento, token emitido, chamada autenticada e autorização efetiva.
- Rotacionar credenciais somente após incidente confirmado e autorização específica do responsável.

### 2.4 — Qualidade técnica
- Registrar versões reais de Python, Node, npm, Git e dependências por ambiente.
- Validar sintaxe YAML com parser disponível; validar esquema separadamente.
- Executar testes existentes em ambiente isolado, sem acesso desnecessário a segredos.
- Separar sintaxe, testes unitários, integração, smoke test e autenticação real.
- Não instalar dependências nem alterar o ambiente sem registrar a necessidade e obter autorização quando a mudança for relevante.

### 2.5 — Licença e atribuição
- Inventariar origem e licença de cada componente relevante.
- Confirmar titularidade ou autorização para licenciar o conteúdo do projeto.
- Preparar MIT somente depois dessa confirmação.
- Manter avisos de terceiros e licenças de dependências conforme aplicável.
- Não criar certificados de autoria, conformidade ou certificação profissional fictícios.

### 2.6 — Publicação GitHub
- Publicar apenas documentação genérica e artefatos sanitizados no repositório público.
- Manter relatórios completos, dados pessoais, detalhes de segurança e evidências privadas em repositório privado controlado pelo responsável.
- Trabalhar em branch de auditoria e abrir pull request quando houver histórico/base apropriados.
- Se o repositório estiver vazio, documentar a decisão de bootstrap e revisar o diff completo antes de publicar mais conteúdo.
- Não importar automaticamente o ZIP Antigravity para este projeto.
- Não habilitar Actions, secrets, deploys ou permissões ampliadas sem aprovação separada.

### 2.7 — Produção gradual
- Gerar checklist de readiness, matriz de riscos, plano de rollback e lista de bloqueios.
- Marcar cada requisito como `PASS`, `FAIL`, `BLOCKED` ou `NOT TESTED`.
- Produção só é aprovada quando os bloqueios críticos forem resolvidos e o responsável humano aprovar explicitamente.

## Saídas obrigatórias

1. `PHASE-2-REPORT.md` com resumo, ambiente, metodologia, resultados, limitações e conclusão.
2. `EVIDENCE-INDEX.md` com referências sanitizadas e hashes.
3. `SECURITY-AND-PRIVACY.md` atualizado com riscos observados.
4. `PRODUCTION-READINESS.md` com critérios e bloqueios.
5. Backlog adaptativo com proposta, evidência que a motivou, prioridade, risco, dependências, critério de aceite e estado.
6. Manifesto de alterações: arquivos criados/alterados, commits, branches e URLs retornadas pela API.

## Condições de parada

Parar e pedir decisão humana se houver: dúvida de titularidade/licença; segredo encontrado; divergência entre fontes; solicitação de acesso adicional; mudança destrutiva; OAuth real não verificável; risco de expor identidade; ou tentativa de alterar outro projeto.
