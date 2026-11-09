# Política de conteúdo para a busca assistida por IA

## Conteúdo permitido na primeira fase

- Documentação técnica aprovada e sanitizada.
- Definições de indicadores e regras de negócio aprovadas.
- Metadados de relatórios, tabelas e colunas, quando autorizados.
- Padrões de ETL sem credenciais nem dados de pessoas.
- Exemplos sintéticos.

## Conteúdo proibido por padrão

- Linhas de bases produtivas.
- Dados pessoais ou sensíveis.
- Tokens, senhas, chaves e strings de conexão.
- URLs privadas, endereços de rede e detalhes de infraestrutura.
- Documentos internos sem aprovação para esse uso.

## Como a IA deve responder

1. Priorizar conteúdo recuperado e aprovado.
2. Apontar documento e seção que sustentam a resposta.
3. Distinguir informação explícita de inferência.
4. Informar quando não houver documentação suficiente.
5. Não inventar regras de negócio, filtros, periodicidade ou responsáveis.
6. Não executar consultas ou ações em produção.

## Avaliação

Manter um conjunto de perguntas de teste com:
- pergunta;
- resposta esperada;
- fontes que deveriam ser recuperadas;
- critérios de aprovação;
- observações sobre respostas incorretas.

A qualidade deve ser avaliada antes de liberar o assistente para usuários.
