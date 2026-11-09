# Procedimento de ETL

> Este modelo substitui instruções dispersas por um registro reproduzível. Nunca documentar senhas, tokens, URLs privadas ou dados reais de pessoas.

## 1. Identificação

- **Nome do processo:**
- **Objetivo:**
- **Responsável pela manutenção:**
- **Frequência / janela de execução:**
- **Criticidade:** (baixa, média, alta)
- **Última revisão:**
- **Versão:**

## 2. Origem e destino

- **Sistema ou fonte lógica:**
- **Tabelas, arquivos ou endpoints necessários:**
- **Destino:** (tabela, arquivo, serviço)
- **Formato de saída:**
- **Granularidade do dado:**
- **Classificação da informação:**

## 3. Pré-requisitos

- **Permissões necessárias (sem descrever credenciais):**
- **Dependências de software:**
- **Variáveis de configuração necessárias:**
- **Ambiente de execução:**

## 4. Execução

1. Preparar o ambiente.
2. Validar parâmetros e período de referência.
3. Executar o processo pelo comando documentado.
4. Registrar identificador da execução e resultado.
5. Não copiar arquivos para locais não autorizados.

**Comando de execução (sem segredos):**

```bash
python pipeline.py --periodo AAAA-MM
```

## 5. Validações

- **Volume esperado ou regra de comparação:**
- **Chaves que devem ser únicas:**
- **Campos obrigatórios:**
- **Tratamento de nulos:**
- **Conferência com fonte de referência:**
- **Critério de aprovação/reprovação:**

## 6. Erros conhecidos e recuperação

| Erro | Causa provável | Ação segura |
|---|---|---|
| Timeout | Consulta ou serviço excedeu o tempo limite | Revisar filtros e plano de execução; testar em janela autorizada |
| Divergência de contagem | Filtros, datas ou granularidade diferentes | Conferir período, fuso, inclusividade e regra de contagem |
| Duplicidade | Chave ou junção inadequada | Verificar cardinalidade e regra de deduplicação |

## 7. Segurança e privacidade

- **Há dados pessoais/sensíveis?**
- **A extração é minimizada?**
- **O destino é autorizado?**
- **Os logs omitem dados pessoais e segredos?**
- **Existe prazo de retenção?**

## 8. Histórico

| Data | Versão | Alteração | Responsável |
|---|---|---|---|
| AAAA-MM-DD | 1.0 | Criação do procedimento | Equipe de dados |
