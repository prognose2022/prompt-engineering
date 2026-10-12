# Critérios de prontidão para produção

Nenhum critério é considerado aprovado sem evidência rastreável.

| Área | Evidência mínima | Estado inicial |
|---|---|---|
| Proveniência | Inventário, origem, hashes e diferenças reconciliadas | BLOCKED |
| Ambiente | Versões e limitações por ambiente documentadas | PARTIAL |
| YAML | Sintaxe e esquema validados separadamente | PARTIAL |
| Testes | Execução reproduzível e resultados anexados | NOT TESTED nesta publicação |
| OAuth | Fluxo real autorizado e chamada autenticada comprovada sem expor tokens | BLOCKED |
| Segurança | Revisão de segredos, permissões e visibilidade | PARTIAL |
| Licença | Titularidade/autorizações confirmadas e avisos corretos | BLOCKED |
| GitHub público | Diff revisado, sem dados privados ou segredos | PARTIAL |
| GitHub privado | Destino e controles de acesso confirmados | BLOCKED |
| Rollback | Procedimento e ponto de restauração testados | NOT TESTED |
| Aprovação humana | Aceite explícito registrado | BLOCKED |

## Definições

- `PASS`: teste realizado e evidência suficiente anexada.
- `FAIL`: teste realizado e requisito não atendido.
- `BLOCKED`: não é possível validar por falta de acesso, autorização ou pré-requisito.
- `NOT TESTED`: teste não executado.
- `PARTIAL`: evidência cobre apenas parte do requisito.

## Gate de liberação

A liberação não deve avançar enquanto titularidade/licença, exposição de segredos, identidade/autorização ou integridade de origem estiverem em `BLOCKED` ou `FAIL`. A decisão final de produção pertence ao responsável humano.

## Resultados observados na auditoria de 12 de outubro de 2026

| Área | Estado observado | Limite |
|---|---|---|
| Proveniência | `BLOCKED` | Cópia local sem histórico Git e divergente da árvore pública; não houve sincronização |
| Ambiente | `PASS` | Ambiente desta sessão documentado; não representa outros ambientes |
| YAML — sintaxe | `PASS` | Três templates carregaram com PyYAML 6.0.3 |
| YAML — esquema | `NOT TESTED` | Schema versionado não localizado |
| Testes automatizados | `NOT TESTED` | Nenhuma suíte da biblioteca foi localizada |
| OAuth e CUE | `BLOCKED` | Sessão autenticada e chamada real não foram comprovadas |
| Segurança | `PARTIAL` | Varredura heurística sem hits, com cobertura limitada |
| Licença | `BLOCKED` | Titularidade/autorizações não confirmadas; licença permanece `PENDING_VERIFICATION` |
| GitHub público | `PARTIAL` | Governança documental presente; biblioteca local não importada nem validada |
| GitHub privado | `NOT TESTED` | Destino e controles não foram confirmados |
| Rollback | `NOT TESTED` | Nenhum exercício executado |
| Aprovação humana | `BLOCKED` | Decisão de titularidade e release pendente |

Esta tabela registra a execução delimitada da auditoria; não altera o registro congelado da Fase 1.
