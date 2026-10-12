# Validação e resultados

## Validação reproduzível

1. Registre versões e caminhos das ferramentas no ambiente utilizado.
2. Valide sintaxe YAML e esquema como verificações distintas.
3. Execute somente os testes existentes e autorizados; registre o comando exato, status, resumo e limitações.
4. Teste adapters nas versões efetivamente instaladas antes de declarar compatibilidade.
5. Não use uma varredura heurística como prova de ausência de segredos.

## Evidência desta auditoria

| Requisito | Resultado | Observação |
|---|---|---|
| Sintaxe dos três templates YAML | `passed` | PyYAML 6.0.3 carregou `backlog.yaml`, `commit-record.yaml` e `snapshot.yaml` |
| Schema YAML | `not_run` | Não foi localizado schema versionado |
| Testes automatizados da biblioteca | `not_run` | Nenhuma suíte de testes está presente no pacote local |
| Compatibilidade dos adapters | `not_run` | Não foram executados em cada ferramenta-alvo |
| OAuth real | `not_run` | Nenhum login ou consentimento foi iniciado |
| Varredura heurística de padrões comuns de credenciais | `passed` com limites | Nenhuma correspondência nos arquivos textuais examinados; isso não prova ausência geral de segredos |

Um resultado `passed` aplica-se apenas à verificação descrita e ao ambiente registrado; não é aprovação de produção.
