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
