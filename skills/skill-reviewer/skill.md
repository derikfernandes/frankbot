---
name: skill-reviewer
description: Use esta skill ao final de toda tarefa para revisar se a skill usada foi suficiente e registrar melhorias necessárias.
triggers:
  - revisar skill
  - melhorar skill
  - aprendizado para skills
  - fim da tarefa
  - skill insuficiente
inputs:
  - skill usada
  - produto gerado
  - problemas encontrados
  - feedback do usuário
outputs:
  - avaliação da skill
  - melhorias recomendadas
  - atualização sugerida
runtime_tools:
  - nenhum na versão inicial
---

# Objetivo

Garantir que o Frankbot melhore continuamente sua biblioteca de skills.

# Procedimento

1. Identificar a skill principal usada.
2. Identificar skills auxiliares usadas.
3. Avaliar se as instruções foram suficientes.
4. Identificar lacunas de procedimento.
5. Identificar necessidade de checklist, template, exemplo ou script.
6. Decidir se a skill deve ser revisada ou se uma nova skill deve ser criada.
7. Registrar recomendação de melhoria.

# Perguntas obrigatórias

- A skill usada foi suficiente?
- O que faltou?
- A lacuna foi de linguagem, estrutura, domínio, dados, verificação ou ferramenta?
- A mesma lacuna pode aparecer novamente?
- Isso deve virar checklist?
- Isso deve virar template?
- Isso deve virar script?
- Isso exige nova skill?

# Saída obrigatória

## Aprendizado para Skills

Skill principal usada:
- [nome]

Skills auxiliares usadas:
- [nomes]

A skill foi suficiente?
- Sim/Não

O que faltou?
- [descrever]

Atualização recomendada:
- Nenhuma / Revisar skill existente / Criar checklist / Criar template / Criar exemplo / Criar script / Criar nova skill

Arquivo sugerido para atualização:
- skills/[nome]/skill.md
