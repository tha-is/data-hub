# Exemplo fictício: geração de resumo mensal

> **Exemplo inteiramente sintético.** Os nomes, prazos, tabelas, comandos e volumes abaixo foram criados para demonstrar o padrão. Não representam sistemas, rotinas, caminhos ou números de uma organização real.

## Objetivo

Gerar um arquivo agregado com a quantidade mensal de solicitações concluídas por região administrativa, para alimentar um painel de acompanhamento.

## Frequência

Mensal, até o segundo dia útil após o fechamento do mês.

## Responsável

Equipe de dados.

## Origem e destino

- **Fonte lógica:** banco analítico de demonstração.
- **Estruturas fictícias:** `fact_requests`, `dim_date` e `dim_region`.
- **Destino:** arquivo Parquet agregado.
- **Granularidade:** mês de referência + região.
- **Dados pessoais:** não devem compor a saída agregada de exemplo.

## Pré-requisitos

- Permissão de leitura no ambiente autorizado.
- Python e dependências definidas no arquivo de projeto.
- Variáveis de conexão fornecidas pelo ambiente seguro; nunca armazenadas no repositório.

## Execução

1. Ativar o ambiente virtual.
2. Informar o mês de referência.
3. Executar o pipeline.
4. Verificar o código de saída e o log técnico.
5. Publicar o arquivo somente no destino aprovado.

Comando ilustrativo:

```bash
python pipeline.py --periodo 2026-10
```

## Validações

- O arquivo foi gerado e pode ser lido.
- O período de referência corresponde ao solicitado.
- A combinação mês + região é única.
- A soma agregada é compatível com uma consulta independente de conferência.
- Valores nulos em campos obrigatórios são tratados conforme regra documentada.

## Problemas conhecidos

- **Tempo limite:** reduzir o escopo temporal, revisar filtros e analisar a consulta antes de aumentar tentativas.
- **Diferença de contagem:** confirmar limites do período, fuso horário, status considerados e granularidade.
- **Duplicidade:** revisar chaves e cardinalidade das junções; não remover duplicatas sem entender a causa.

## Observação

Este exemplo é um ponto de partida. Antes de adaptar a uma rotina real, validar regras de negócio, permissões, classificação e destino com os responsáveis.
