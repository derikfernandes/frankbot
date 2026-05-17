---
name: qa-controladoria
description: Use esta skill para revisar criticamente qualquer saída final do Frankbot, verificando aderência à spec, cautela institucional, evidências, lacunas e necessidade de evolução de skills.
triggers:
  - revisar entrega
  - validar relatório
  - qa
  - verificar qualidade
  - revisão técnica
inputs:
  - produto final
  - specs relevantes
  - critérios de aceite
  - tests.yaml
outputs:
  - aprovado
  - aprovado com ressalvas
  - reprovado
  - ajustes necessários
runtime_tools:
  - nenhum na versão inicial
---

# Objetivo

Atuar como verificador técnico da entrega, procurando inconsistências antes que o documento seja aceito.

# Procedimento

1. Comparar a entrega com o objetivo do usuário.
2. Verificar se o produto respeita o contrato de saída.
3. Procurar afirmações sem evidência suficiente.
4. Verificar se fatos, inferências, riscos e recomendações foram separados.
5. Verificar linguagem institucional e cautelosa.
6. Conferir se há lacunas importantes não declaradas.
7. Conferir se há itens fora do escopo.
8. Classificar a entrega.
9. Avaliar se alguma skill precisa ser criada ou revisada.

# Classificação

## Aprovado

A entrega atende aos critérios de aceite e não possui ressalvas relevantes.

## Aprovado com ressalvas

A entrega é útil, mas possui ajustes recomendados.

## Reprovado

A entrega viola critérios essenciais, cria informação não fornecida, usa tom inadequado ou não responde ao objetivo.

# Checklist obrigatório

- [ ] Responde ao objetivo?
- [ ] Usa fontes ou deixa claro quando não há fonte?
- [ ] Separa fato de inferência?
- [ ] Evita conclusão sem evidência?
- [ ] Indica lacunas?
- [ ] Possui recomendações acionáveis?
- [ ] Respeita fora de escopo?
- [ ] Avalia aprendizado para skills?

# Saída obrigatória

## Veredito

[Aprovado / Aprovado com ressalvas / Reprovado]

## Problemas encontrados

- ...

## Ajustes necessários

- ...

## Aprendizado para Skills

Skill foi suficiente?
- Sim/Não

Atualização recomendada:
- Nenhuma / Revisar skill / Criar nova skill / Criar checklist / Criar template / Criar script
