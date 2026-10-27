# DIO-Planilhas-Organizador-Imposto-Renda



\# 📊 Sistema de Coleta \& Declaração de Rendimentos Pessoais



Este projeto foi desenvolvido para padronizar e automatizar a coleta de dados pessoais, informes de rendimentos bancários e notas/extratos para a elaboração do Imposto de Renda (IRPF) ou controle de patrimônio individual.



\---



\## 📌 Índice



\- \[Visão Geral](#-visão-geral)

\- \[Estrutura da Planilha](#-estrutura-da-planilha)

\- \[Bancos Suportados](#-bancos-suportados)

\- \[Fluxo de Preenchimento](#-fluxo-de-preenchimento)

\- \[Requisitos do Sistema](#-requisitos-do-sistema)

\- \[Como Utilizar](#-como-utilizar)

\- \[Contribuição](#-contribuição)



\---



\## 🔍 Visão Geral



O objetivo principal da aplicação/planilha é organizar e consolidar as informações do contribuinte em um único local, permitindo o acompanhamento do saldo consolidado de contas e movimentações bancárias do exercício fiscal.



\*\*Principais Recursos:\*\*

\- 👤 Cadastramento simplificado de dados pessoais do titular e dependentes.

\- 🏦 Lançamento de \*\*Informes de Rendimentos Bancários\*\* com cálculo automático do valor total acumulado.

\- 💵 Registro detalhado de \*\*Entradas de Receita\*\* (Holerites, Notas Bancárias e Extratos por Categoria).

\- 📋 Tabela de validação/autocomplete integrada contendo códigos das principais instituições financeiras registradas no Banco Central do Brasil.



\---



\## 📂 Estrutura da Planilha (`application.xlsx`)



A planilha principal está organizada nas seguintes abas (\*worksheets\*):



| Aba | Descrição | Dados Principais |

| :--- | :--- | :--- |

| \*\*`TITULAR`\*\* | Cadastro dos dados do contribuinte | Nome, CPF, Data de Nascimento, Título de Eleitor, Endereço, Cônjuge, Residentes no Exterior e Alterações. |

| \*\*`INFORMES`\*\* | Consolidação de Saldos/Rendimentos | Instituição Financeira, Valor Atual Acumulado, Anexo do PDF do Informe e Totalizador Geral (`SUM`). |

| \*\*`NOTAS`\*\* | Registro de Extratos e Holerites | Data do Lançamento, Categoria da Receita (ex: \*HOLERITE\*) e Valor de Entrada. |

| \*\*`TABELAS`\*\* | Tabela Auxiliar de Domínios | Lista padronizada dos bancos brasileiros (Código + Nome Fantasia) para consulta/validação de dados. |



\---



\## 🏦 Bancos Suportados (`BANCOS.xlsx`)



O sistema conta com um cadastro de mais de 50 instituições bancárias e fintechs padronizadas. Entre elas:



\- \*\*Bancos Tradicionais:\*\* Banco do Brasil (001), Caixa Econômica Federal (104), Bradesco (237), Santander (033), Itaú Unibanco (341), Safra (422).

\- \*\*Digital \& Fintechs:\*\* Nubank (260), PicPay (380), C6 Bank (336), Inter (077), Neon (735), PagBank (290), Stone (197).

\- \*\*Corretoras \& Investimentos:\*\* XP Investimentos (102), BTG Pactual (208), Modal (746).



\---



\## 📝 Fluxo de Preenchimento



```mermaid

flowchart TD

&#x20;   A\[Aba: TITULAR] -->|Preencher dados pessoais| B\[Aba: INFORMES]

&#x20;   B -->|Inserir saldos bancários e anexar PDFs| C\[Aba: NOTAS]

&#x20;   C -->|Registrar entradas mensais e holerites| D\[Totalização \& Consolidação]

´´´

