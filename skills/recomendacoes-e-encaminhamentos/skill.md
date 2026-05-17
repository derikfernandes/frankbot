---
name: recomendacoes-e-encaminhamentos
description: Use esta skill para transformar achados tecnicos em recomendacoes objetivas, solucoes sugeridas, alternativas de gestao e encaminhamentos institucionais.
triggers:
  - fazer recomendacoes
  - solucoes sugeridas
  - encaminhamentos
  - providencias
  - plano de acao
inputs:
  - achados tecnicos
  - riscos identificados
  - impactos estimados
  - contexto do caso
outputs:
  - recomendacoes acionaveis
  - solucoes sugeridas
  - vantagens e desvantagens
  - evidencias de cumprimento
runtime_tools:
  - nenhum na versao inicial
---

# Objetivo

Produzir recomendacoes claras, proporcionais e acionaveis, conectadas aos achados da analise tecnica.

# Procedimento

1. Ler os achados tecnicos.
2. Identificar o problema que cada achado revela.
3. Identificar o risco ou impacto associado.
4. Formular recomendacao pratica.
5. Quando houver alternativas, montar quadro comparativo.
6. Indicar evidencia esperada para comprovar atendimento.
7. Evitar recomendacoes genericas.
8. Encaminhar para QA.
9. Ao final, revisar se esta skill precisa ser melhorada.

# Verbos recomendados

- avaliar a possibilidade de;
- readequar;
- reavaliar;
- implementar;
- redesenhar;
- promover;
- instalar;
- estabelecer regra;
- exigir comprovacao;
- aprimorar;
- aperfeicoar.

# Evitar

- melhorar o contrato;
- resolver o problema;
- acompanhar melhor;
- tomar providencias;
- verificar a situacao.

# Estrutura de recomendacao

```text
Recomenda-se [acao concreta], com o objetivo de [resultado esperado], considerando [evidencia/achado].
Como evidencia de atendimento, sugere-se [documento, dado, relatorio ou comprovacao].
```

# Quadro comparativo de solucoes

Quando houver mais de uma alternativa, usar:

| Solucao | Vantagens | Desvantagens | Risco mitigado | Observacao |
|---|---|---|---|---|

# Aprendizado obrigatorio

Ao final da tarefa, responder:

- As recomendacoes foram acionaveis?
- Faltou padrao para algum tipo de encaminhamento?
- Deve ser criado novo template?
- Deve ser criada nova skill?
