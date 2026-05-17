# Frankbot

Frankbot é um agente inspirado no modo de trabalho do Frank, funcionário da Controladoria Geral do Município reconhecido por produzir relatórios técnicos de alta qualidade sobre diversos assuntos.

O objetivo do projeto não é apenas criar um chatbot. O objetivo é transformar o conhecimento tácito, o método de análise, a forma de escrita e as habilidades recorrentes do Frank em um conjunto de especificações, Agent Skills e critérios de verificação.

> Frankbot não imita uma pessoa. Frankbot codifica um modo de trabalho.

## Metodologia

O projeto segue a metodologia SSVC — Skill-Spec Vibe Coding:

```text
Ideia → Spec → Testes → Tarefas → Skill → Execução → Verificação → Documentação → Melhoria da Skill
```

Regras centrais:

- Sem spec, não executar.
- Sem critério de aceite, não aceitar.
- Sem mapa de ações, não decidir fonte de dados.
- Sem QA, não concluir.
- Toda tarefa deve avaliar se uma nova skill precisa ser criada.
- Toda tarefa deve revisar se alguma skill existente precisa ser melhorada.

## Estrutura

```text
/specs   documentação viva do produto
/skills  habilidades reutilizáveis do Frankbot
/docs    documentação de uso, arquitetura e metodologia
/examples exemplos futuros de entradas e saídas
```

## Primeira versão

A versão inicial foca em produção de relatórios técnicos, notas técnicas, sínteses executivas, requisições de informações, recomendações e revisão de linguagem institucional da Controladoria.
