# 05 — Action Routing Map

## Objetivo

Definir onde o Frankbot deve buscar informações e qual skill deve acionar para cada tipo de ação.

O Frankbot não deve adivinhar fonte de dados. Quando uma informação não estiver disponível, deve declarar lacuna.

| Ação | Origem | Fonte de dados | Skill principal | Saída esperada |
|---|---|---|---|---|
| Ler processo | Upload ou texto do usuário | Arquivos anexos | leitura-processual | fatos, partes, objeto e lacunas |
| Analisar contrato | Upload ou texto do usuário | contrato e anexos | analise-tecnica-controladoria | riscos, obrigações e pontos de atenção |
| Produzir relatório | Usuário + documentos | informações consolidadas | redacao-relatorio-tecnico | relatório estruturado |
| Revisar linguagem | Texto produzido | minuta | linguagem-institucional | texto revisado |
| Formular recomendação | Achados | análise técnica | recomendacoes-e-encaminhamentos | recomendações objetivas |
| Validar entrega | Produto final | spec + checklist | qa-controladoria | aprovado, aprovado com ressalvas ou reprovado |
| Criar nova skill | Lacuna identificada | tarefa atual + lições aprendidas | skill-creator | nova skill documentada |
| Revisar skill existente | Lacuna em skill usada | skill atual + resultado da tarefa | skill-reviewer | melhoria registrada |

## Regras de roteamento

1. Se a tarefa envolver documentos extensos, começar por `leitura-processual`.
2. Se a tarefa envolver riscos, conformidade ou achados, usar `analise-tecnica-controladoria`.
3. Se a tarefa exigir documento final, usar `redacao-relatorio-tecnico`.
4. Se a tarefa envolver tom, cautela ou clareza, usar `linguagem-institucional`.
5. Se a tarefa exigir providências, usar `recomendacoes-e-encaminhamentos`.
6. Toda entrega final deve passar por `qa-controladoria`.
7. Toda tarefa deve terminar avaliando `skill-creator` e `skill-reviewer`.
