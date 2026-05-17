---
name: skill-creator
description: Use esta skill quando uma tarefa exigir procedimento novo, recorrente ou especializado que ainda não esteja coberto pelas skills existentes.
triggers:
  - nova habilidade necessária
  - criar skill
  - procedimento novo
  - tarefa recorrente sem skill
  - lacuna de skill
inputs:
  - descrição da tarefa
  - lacuna identificada
  - skills existentes
  - resultado esperado
outputs:
  - nova pasta de skill proposta
  - skill.md inicial
  - gatilhos
  - entradas e saídas
runtime_tools:
  - nenhum na versão inicial
---

# Objetivo

Criar uma nova skill sempre que o Frankbot encontrar uma demanda relevante que não esteja bem coberta pelas skills existentes.

# Quando criar nova skill

Criar ou propor nova skill quando:

1. a tarefa exigir procedimento específico ainda não documentado;
2. o mesmo tipo de tarefa aparecer três vezes;
3. a tarefa depender de checklist próprio;
4. a tarefa exigir template específico;
5. a execução atual depender de muitas instruções improvisadas;
6. uma skill existente ficar ampla demais.

# Procedimento

1. Descrever a lacuna encontrada.
2. Verificar se alguma skill existente pode ser ampliada.
3. Se a lacuna for específica e recorrente, propor nova skill.
4. Definir nome curto da skill.
5. Definir description, triggers, inputs, outputs e runtime_tools.
6. Criar procedimento inicial.
7. Criar checklist mínimo.
8. Registrar exemplos futuros necessários.

# Estrutura mínima

```text
skills/nome-da-skill/
  skill.md
  checklist.md
  examples/
  templates/
```

# Saída esperada

## Nova skill necessária?

Sim/Não

## Nome sugerido

[nome-da-skill]

## Motivo

[por que a skill é necessária]

## Conteúdo inicial

[rascunho do skill.md]
