# Carta de Confiança dos Dados — BITCOIN

**Projeto:** BITCOIN  
**Repositório:** carlos-andrade/BITCOIN  
**Data de criação:** 24/09/2026  
**Status:** Norma oficial de confiabilidade e auditabilidade

## 1. Objetivo

Esta carta estabelece as regras mínimas para que dados, séries históricas, métricas, análises e resultados registrados no repositório possam ser considerados **rastreáveis, reproduzíveis, verificáveis e adequados ao uso declarado**.

Confiança não significa que um dado seja necessariamente verdadeiro. Significa que sua origem, transformação, integridade, metodologia e limitações podem ser examinadas.

## 2. Hierarquia das fontes

Priorizar, nesta ordem:

1. Fontes primárias oficiais.
2. Documentação técnica oficial.
3. Publicações acadêmicas revisadas por pares.
4. Bases de dados institucionais reconhecidas.
5. Provedores de dados com metodologia documentada.
6. Fontes secundárias, somente quando necessárias e identificadas.
7. Mídias sociais, fóruns e conteúdo não verificável não devem ser tratados como fonte primária de evidência.

Quando fontes confiáveis divergirem, a divergência deve ser registrada, não ocultada.

## 3. Identificação obrigatória

Todo conjunto de dados deve registrar, quando disponível:

- nome da fonte;
- URL ou identificador da fonte;
- data e hora de obtenção;
- período coberto;
- frequência;
- unidade de medida;
- fuso horário;
- ativo, mercado ou população;
- versão da fonte ou arquivo;
- método de aquisição;
- responsável pelo processamento;
- hash do arquivo original, quando aplicável.

## 4. Integridade

O arquivo original deve ser preservado sempre que legal e tecnicamente possível.

Dados brutos não devem ser sobrescritos por dados tratados.

Toda transformação deve gerar uma etapa identificável e documentada.

Quando possível, utilizar hashes criptográficos, checksums ou mecanismos equivalentes para comprovar integridade.

## 5. Rastreabilidade

Cada número publicado deve permitir responder:

**De onde veio? Quando foi obtido? Como foi transformado? Qual código o processou? Qual versão produziu o resultado?**

Nenhum resultado crítico deve depender de transformação manual não documentada.

## 6. Reprodutibilidade

Scripts utilizados para ingestão, limpeza, normalização, cálculo, agregação ou validação devem ser versionados.

A documentação deve registrar:

- entrada;
- processamento;
- parâmetros;
- saída esperada;
- saída obtida;
- ambiente relevante;
- versão do código.

Sempre que possível, outra pessoa deve conseguir reproduzir o resultado a partir dos arquivos e instruções disponíveis.

## 7. Validação

Antes de publicar dados derivados, executar validações adequadas ao conjunto, incluindo quando aplicável:

- schema;
- tipos;
- datas;
- duplicidades;
- valores ausentes;
- valores inválidos;
- continuidade temporal;
- ordenação;
- unidades;
- preços;
- volumes;
- identificadores;
- consistência entre campos;
- consistência entre fontes;
- outliers e mudanças estruturais.

Falhas de validação não devem ser silenciosamente descartadas.

## 8. Dados financeiros e de mercado

Para Bitcoin e mercados relacionados, distinguir explicitamente:

- preço spot;
- preço de índice;
- preço de contrato futuro;
- preço de perpétuo;
- preço de fechamento;
- preço de referência;
- volume reportado;
- volume estimado;
- open interest;
- funding;
- liquidações;
- dados on-chain;
- métricas derivadas.

Não misturar séries com definições diferentes sem documentar a transformação.

## 9. Dados on-chain

Métricas on-chain devem informar, quando aplicável:

- blockchain;
- altura do bloco;
- timestamp;
- método de indexação;
- entidade ou clusterização utilizada;
- definição da métrica;
- tratamento de endereços;
- tratamento de coinbase;
- tratamento de forks/reorgs;
- janela temporal;
- limitações conhecidas.

Uma métrica derivada não deve ser apresentada como fato diretamente observado.

## 10. Cálculos e métricas

Toda métrica calculada deve possuir:

- definição matemática;
- fórmula;
- parâmetros;
- janela;
- frequência;
- unidade;
- tratamento de dados ausentes;
- tratamento de outliers;
- código ou metodologia reproduzível.

Percentuais, retornos, volatilidade, drawdown, correlações e demais estatísticas devem indicar claramente a amostra e o período.

## 11. Fatos, dados, hipóteses e opiniões

O repositório deve distinguir quatro categorias:

**Fato:** informação diretamente sustentada por fonte verificável.

**Dado:** observação ou valor proveniente de uma fonte identificada.

**Hipótese:** explicação ou proposição ainda não demonstrada.

**Opinião:** interpretação ou julgamento analítico.

Nenhuma hipótese ou opinião deve ser apresentada como fato.

## 12. Ausência de evidência

Quando não houver evidência suficiente, registrar:

- "não verificado";
- "evidência insuficiente";
- "estimativa";
- "proxy";
- "hipótese";
- ou classificação equivalente.

É preferível declarar incerteza a preencher lacunas com inferência não documentada.

## 13. Correções

Erros encontrados devem ser corrigidos de forma rastreável.

Não apagar silenciosamente o histórico relevante.

Registrar:

- erro identificado;
- impacto;
- causa conhecida;
- correção;
- data;
- versão afetada;
- validação posterior.

Quando uma publicação anterior tiver sido materialmente afetada, documentar explicitamente a correção.

## 14. Versionamento

Todo resultado relevante deve ser associado a uma versão identificável do código e dos dados.

Commits, tags, hashes ou identificadores equivalentes devem ser utilizados para permitir auditoria histórica.

Alterações de metodologia devem gerar documentação própria.

## 15. Independência das fontes

Quando uma conclusão depender de múltiplas fontes, verificar se elas são realmente independentes.

Reprodução do mesmo dado por diversos sites não constitui confirmação independente se todos derivam da mesma fonte original.

## 16. Conflitos entre fontes

Quando duas fontes apresentarem valores diferentes:

1. identificar as definições;
2. verificar horários e fusos;
3. verificar metodologia;
4. verificar revisões;
5. verificar universo e amostra;
6. registrar ambos os valores quando necessário;
7. explicar por que um foi utilizado.

Não escolher silenciosamente o valor mais conveniente.

## 17. Dados estimados

Estimativas devem ser explicitamente rotuladas.

Devem conter:

- método;
- premissas;
- intervalo ou margem de incerteza, quando possível;
- fonte das premissas;
- limitações.

Estimativa não deve ser confundida com observação.

## 18. Segurança e manipulação

Dados provenientes de fontes externas devem ser tratados como não confiáveis até validação.

Scripts de ingestão devem evitar alteração silenciosa de dados.

Credenciais, tokens, chaves privadas e informações sensíveis nunca devem ser armazenados no repositório.

## 19. Limitações

Todo conjunto relevante deve documentar limitações conhecidas, incluindo:

- cobertura;
- atrasos;
- revisões;
- survivorship bias;
- look-ahead bias;
- viés de seleção;
- mudanças metodológicas;
- diferenças de timezone;
- gaps;
- forks;
- problemas de liquidez;
- limitações do provedor.

## 20. Regra de ouro

**Nenhum dado é considerado confiável apenas porque está no GitHub.**

A confiança deve resultar da combinação de:

**origem + integridade + definição + metodologia + rastreabilidade + validação + reprodutibilidade + versionamento + transparência sobre limitações.**

## 21. Critério de publicação

Um dado ou resultado pode ser classificado como **VALIDADO** somente quando houver evidência suficiente para sustentar sua definição, origem, integridade e processo de validação.

Classificações recomendadas:

- **RAW** — dado original preservado.
- **INGESTED** — dado adquirido e identificado.
- **NORMALIZED** — dado transformado conforme metodologia documentada.
- **VALIDATED** — passou pelas validações definidas.
- **REPRODUCIBLE** — processo pode ser reproduzido.
- **AUDITED** — revisão adicional documentada.
- **ESTIMATED** — resultado estimado.
- **UNVERIFIED** — ainda não validado.
- **DEPRECATED** — não deve mais ser utilizado.

## 22. Princípio final

O repositório BITCOIN deve privilegiar **evidência sobre narrativa, método sobre conveniência, rastreabilidade sobre autoridade e transparência sobre falsa precisão**.

Esta carta constitui a referência oficial para avaliar a confiança dos dados gravados no projeto BITCOIN.