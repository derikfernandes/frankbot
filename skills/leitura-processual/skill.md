---
name: leitura-processual
description: Use esta skill para ler processos, contratos, planos de trabalho, notas tecnicas, relatorios, prestacoes de contas e documentos administrativos, extraindo objeto, fatos, fontes, cronologia, lacunas e pontos de atencao.
triggers:
  - ler processo
  - entender documento
  - resumir contrato
  - analisar anexos
  - extrair fatos
  - mapear documentos
inputs:
  - arquivos enviados pelo usuario
  - texto do processo
  - contrato
  - plano de trabalho
  - relatorio
outputs:
  - objeto do caso
  - partes envolvidas
  - fatos principais
  - cronologia
  - documentos relevantes
  - lacunas
  - pontos de atencao
runtime_tools:
  - nenhum na versao inicial
---

# Objetivo

Transformar documentos administrativos em uma base organizada de fatos, evidencias, lacunas e pontos de atencao para posterior analise tecnica.

# Procedimento

1. Identificar o tipo de documento.
2. Identificar o objeto principal.
3. Identificar orgaos, entidades, contratados ou setores envolvidos.
4. Extrair dados essenciais: numero de contrato, objeto, valor, periodo, metas, responsaveis e fontes.
5. Criar cronologia, quando houver datas relevantes.
6. Separar fatos de interpretacoes.
7. Identificar tabelas, graficos e fluxos relevantes.
8. Apontar lacunas de informacao.
9. Sugerir quais skills devem ser acionadas em seguida.

# Saida recomendada

## Objeto

[descrever]

## Fontes analisadas

- [fonte 1]
- [fonte 2]

## Fatos principais

- [fato 1]
- [fato 2]

## Dados relevantes

- [dado 1]
- [dado 2]

## Lacunas

- [lacuna 1]
- [lacuna 2]

## Pontos de atencao

- [ponto 1]
- [ponto 2]

## Skills recomendadas para proxima etapa

- [skill]

# Regras

Nao criar dado que nao esteja no documento.
Nao transformar suspeita em conclusao.
Quando o documento possuir graficos ou tabelas, indicar que eles devem ser considerados na analise.

# Aprendizado obrigatorio

Ao final da tarefa, avaliar se esta skill precisa de novo checklist, template, exemplo ou script.
