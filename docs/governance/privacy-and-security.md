# Governança, privacidade e segurança

## Regra fundamental

O Data Hub deve catalogar conhecimento técnico e metadados, não replicar bases operacionais. Dados pessoais e sensíveis devem permanecer fora dos documentos e exemplos sempre que não forem estritamente necessários.

## Classificação sugerida

| Classe | Exemplos | Tratamento no Data Hub |
|---|---|---|
| Público | documentação pública de ferramentas | Pode ser usado após verificação |
| Interno | padrões técnicos sem dados pessoais | Somente com autorização |
| Confidencial | arquitetura interna, URLs privadas, detalhes de acesso | Não incluir no GitHub pessoal; exigir ambiente aprovado |
| Pessoal/sensível | identificadores, dados de saúde, registros individuais | Não incluir em exemplos, prompts ou base de conhecimento |

A classificação definitiva deve seguir a política da organização.

## Controles mínimos antes de uso real

- Aprovação formal da organização para hospedagem, titularidade e uso de ferramentas externas.
- Controle de acesso por usuário e função.
- Segredos fora do código-fonte, usando variáveis de ambiente ou cofre aprovado.
- Criptografia em trânsito e em repouso, conforme ambiente.
- Logs sem conteúdo sensível, tokens, senhas ou dados pessoais.
- Registro de alterações, autoria, data e versão dos documentos.
- Política de retenção e descarte.
- Backup e procedimento de restauração testados.
- Revisão de permissões e acessos periodicamente.

## Uso de IA

Antes de enviar qualquer conteúdo a um provedor externo, validar contrato, região de processamento, retenção, uso para treinamento, controles de acesso e aprovação institucional. Não presumir que uma API é adequada apenas por ser paga ou empresarial.

A primeira versão da busca deve operar sobre documentos previamente aprovados e preferencialmente sanitizados. A IA deve citar as fontes utilizadas e declarar quando não encontrar informação suficiente.

## Checklist de publicação

- [ ] Não há nomes de pessoas, e-mails, telefones ou identificadores reais.
- [ ] Não há dados pessoais ou sensíveis, nem amostras extraídas de produção.
- [ ] Não há URLs privadas, hostnames, IPs, caminhos de rede ou nomes internos de sistemas.
- [ ] Não há credenciais, tokens, chaves ou arquivos de configuração secretos.
- [ ] A organização autorizou o local de hospedagem e a publicação.
