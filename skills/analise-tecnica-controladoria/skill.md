---
name: analise-tecnica-controladoria
description: Use esta skill para analisar contratos, planos de trabalho, execucao de servicos, prestacoes de contas, riscos, achados, economicidade e eficiencia na aplicacao de recursos publicos.
triggers:
  - analisar contrato
  - avaliar execucao contratual
  - identificar riscos
  - analisar economicidade
  - avaliar plano de trabalho
  - analisar prestacao de contas
  - nota tecnica
inputs:
  - descricao do caso
  - contrato ou plano de trabalho
  - dados financeiros
  - dados operacionais
  - relatorios de fiscalizacao
  - prestacoes de contas
outputs:
  - achados tecnicos
  - riscos identificados
  - impactos estimados
  - solucoes sugeridas
  - recomendacoes
runtime_tools:
  - nenhum na versao inicial
---

# Objetivo

Produzir analise tecnica de Controladoria com foco em eficiencia, economicidade, conformidade, riscos, impactos e melhoria da gestao publica.

# Procedimento

1. Identificar o objeto analisado.
2. Identificar documentos e dados disponiveis.
3. Separar a analise por blocos tematicos.
4. Levantar fatos observados.
5. Associar cada fato a evidencia ou dado.
6. Identificar risco financeiro, operacional, juridico ou de desempenho.
7. Mensurar impacto sempre que houver dados suficientes.
8. Apontar lacunas de informacao.
9. Formular solucoes ou alternativas.
10. Encaminhar achados para a skill de recomendacoes, quando necessario.
11. Encaminhar texto final para QA.
12. Ao final, revisar se esta skill precisa ser melhorada.

# Blocos de analise recomendados

## Para contrato de servico

- visao geral do contrato;
- fase de planejamento ou licitacao;
- execucao contratual;
- indicadores de desempenho;
- custos e desperdicios;
- solucoes sugeridas;
- recomendacoes.

## Para contrato de gestao

- visao geral do contrato;
- plano de trabalho;
- metas e objetivos;
- execucao do contrato;
- prestacao de contas;
- economicidade;
- fiscalizacao;
- solucoes sugeridas.

# Padrao de achado

Cada achado deve conter:

- fato observado;
- evidencia;
- explicacao tecnica;
- impacto;
- risco;
- possivel solucao.

# Regras de cautela

Nao concluir alem das evidencias disponiveis.

Nao afirmar irregularidade definitiva quando houver apenas indício, inconsistencia ou fragilidade.

Quando faltar dado, registrar lacuna.

# Perguntas orientadoras

- O objeto foi bem planejado?
- As metas sao claras e mensuraveis?
- Ha detalhamento suficiente do custo?
- O modelo de execucao gera incentivos adequados?
- Ha risco de desperdicio?
- Ha diferenca relevante entre previsto e executado?
- Ha concentracao excessiva de execucao?
- Ha fragilidade de fiscalizacao?
- A recomendacao e acionavel?

# Aprendizado obrigatorio

Ao final da tarefa, responder:

- A skill foi suficiente?
- Surgiu padrao novo de analise?
- Deve ser criada uma skill especifica?
- Deve ser criado checklist, template ou script?
