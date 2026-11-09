# Visão geral do Data Hub

## Problema que queremos resolver

O conhecimento de BI e de processos de dados costuma ficar disperso em arquivos, scripts, mensagens e na memória de quem executa as tarefas. O Data Hub pretende organizar esse conhecimento sem exigir documentação extensa de cada relatório.

## Escopo inicial

### 1. Inventário de BI
Registro resumido de relatórios, áreas responsáveis, fontes, periodicidade, classificação e localização. O inventário não substitui a documentação detalhada dos indicadores.

### 2. Biblioteca de indicadores
Registro dos indicadores mais importantes e reutilizáveis: definição, regra de negócio, medida DAX, unidade, periodicidade, dimensões e ressalvas.

### 3. Catálogo de ETL
Procedimentos padronizados para extrações, integrações, transformações, validações e publicação de arquivos ou tabelas.

### 4. Padrões de Power BI
Temas JSON, paleta, tipografia, orientações de uso e, futuramente, modelos de relatório.

### 5. Busca assistida por IA (fase posterior)
Busca em conteúdo aprovado, com respostas fundamentadas em fontes. A IA não deve executar consultas em bases produtivas nem acessar dados pessoais por padrão.

## Fora do escopo inicial

- Substituir ferramentas corporativas de BI, ETL ou governança.
- Centralizar dados operacionais ou cópias de bases produtivas.
- Treinar um modelo de IA com dados internos.
- Executar alterações em sistemas ou bancos de produção.

## Arquitetura planejada

```text
Frontend: React + TypeScript + Tailwind
        |
        v
Backend: Python + FastAPI
        |
        +--> PostgreSQL (metadados e catálogo)
        +--> armazenamento controlado de documentos
        +--> camada de busca/RAG (fase posterior)
        +--> adaptadores para provedores de IA (fase posterior)
```

A arquitetura deve manter regras determinísticas no backend. A IA pode localizar, resumir e explicar informações documentadas, mas não deve inventar regras ausentes.

## Decisões ainda abertas

- Onde o sistema poderá ser hospedado (máquina local, servidor corporativo ou nuvem aprovada).
- Identidade, autenticação e autorização.
- Provedor de IA e condições contratuais de tratamento de dados.
- Estratégia de backup, retenção e auditoria.
- Formatos e versões de arquivos Power BI que serão suportados.
