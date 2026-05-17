# 01 — Domain Model

## Entidades principais

### Caso

Representa o assunto submetido ao Frankbot.

Campos conceituais:

- `id`: identificador do caso;
- `titulo`: título resumido;
- `tipo`: tipo de demanda;
- `origem`: origem da demanda;
- `secretaria_relacionada`: órgão ou unidade envolvida;
- `descricao`: descrição inicial;
- `documentos_anexos`: documentos fornecidos;
- `dados_anexos`: planilhas ou bases de dados fornecidas;
- `objetivo_da_analise`: o que se pretende responder;
- `publico_destinatario`: quem receberá o documento final;
- `nivel_de_sensibilidade`: baixo, médio ou alto.

### Documento de entrada

Representa qualquer arquivo usado como fonte.

Tipos possíveis:

- processo administrativo;
- contrato;
- relatório anterior;
- planilha;
- imagem;
- despacho;
- manifestação;
- parecer;
- denúncia;
- reclamação do 156;
- notícia;
- base de dados operacional.

### Evidência

Representa um fato extraído de fonte disponível.

Campos conceituais:

- `fonte`;
- `trecho_relevante`;
- `tipo_de_evidencia`;
- `grau_de_confiabilidade`;
- `observacao`.

Tipos de evidência:

- documental;
- tabular;
- declaratória;
- fotográfica;
- sistêmica;
- normativa;
- histórica.

### Achado

Representa uma constatação técnica construída a partir das evidências.

Um achado deve conter:

- situação observada;
- evidência que sustenta;
- possível impacto;
- grau de risco;
- lacunas de informação;
- recomendação associada, quando houver.

### Recomendação

Representa uma providência sugerida.

Uma recomendação deve conter:

- ação recomendada;
- responsável sugerido;
- justificativa;
- evidência necessária para comprovar atendimento;
- prazo, quando aplicável;
- risco mitigado.

### Produto final

Tipos de saída do Frankbot:

- relatório técnico;
- nota técnica;
- síntese executiva;
- despacho;
- resposta institucional;
- requisição de informações;
- matriz de achados;
- checklist de verificação;
- minuta de encaminhamento;
- resumo para autoridade.
