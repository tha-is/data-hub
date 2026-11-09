# Data Hub

Plataforma interna para organizar conhecimento de BI, padronizar processos de ETL e facilitar a consulta a documentação técnica e de negócio.

> **Estado do projeto:** estrutura inicial de documentação. Ainda não há aplicação, autenticação ou integração com IA implementadas.

## Objetivos

- Manter um inventário leve de relatórios, fontes e responsáveis.
- Documentar indicadores relevantes com suas regras de negócio e medidas DAX.
- Catalogar padrões e procedimentos de ETL.
- Disponibilizar padrões visuais para Power BI.
- Futuramente, oferecer busca assistida por IA sobre conteúdo aprovado, sempre apresentando fontes.

## Princípios

1. **Privacidade por padrão:** não armazenar dados pessoais ou sensíveis nos exemplos, documentos ou prompts.
2. **Rastreabilidade:** registrar fonte, responsável, revisão e versão.
3. **Separar fato de interpretação:** conteúdo documentado deve ser distinguido de sugestões geradas por IA.
4. **Pequenos passos:** automatizar somente depois de entender e validar o processo manual.
5. **Portabilidade:** desenvolver localmente com possibilidade de migração para ambiente corporativo aprovado.

## Estrutura

```text
data-hub/
├── docs/
│   ├── architecture/
│   ├── governance/
│   ├── bi/
│   └── etl/
├── examples/
│   └── synthetic/
├── powerbi/
│   └── themes/
├── backend/
├── frontend/
├── database/
├── .github/
├── .gitignore
└── README.md
```

As pastas de aplicação serão preenchidas nas próximas etapas.

## Documentação inicial

- [Visão e escopo](docs/architecture/overview.md)
- [Governança e LGPD](docs/governance/privacy-and-security.md)
- [Inventário de BI](docs/bi/report-inventory-template.md)
- [Catálogo de indicadores](docs/bi/indicator-template.md)
- [Padrão de ETL](docs/etl/etl-procedure-template.md)
- [Exemplo fictício de ETL](docs/etl/example-monthly-summary.md)
- [Política de conhecimento para IA](docs/governance/ai-knowledge-policy.md)

## Desenvolvimento

A stack planejada é React + TypeScript + Tailwind no frontend, Python + FastAPI no backend e PostgreSQL para persistência. A escolha de hospedagem, provedor de IA e autenticação será feita após validar os requisitos e as autorizações do ambiente onde o sistema será utilizado.

## Segurança antes do primeiro push

- Confirme se a organização permite hospedar o projeto em uma conta pessoal do GitHub.
- Não envie dados reais, documentos internos, nomes de sistemas, URLs privadas, endereços de rede, credenciais ou código pertencente à empresa sem autorização.
- Use somente dados sintéticos neste repositório.
- Configure o repositório como privado enquanto o escopo e a titularidade estiverem sendo definidos.
- Um repositório privado não substitui aprovação corporativa nem controles de segurança.
