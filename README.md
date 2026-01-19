# Limpeza e Padronização de Dados de Vendas (Excel)

## Objetivo
Realizar a limpeza e padronização de uma base de dados de vendas originalmente em formato CSV, corrigindo inconsistências e preparando os dados para análises futuras, sem perda desnecessária de informações.

## Base original
A base original (`Dados Sujos.csv`) apresentava diversos problemas comuns em dados reais, como:

- Campos vazios
- Formatação inconsistente de datas e valores
- Erros de cálculo (`#NÚM!`)
- E-mails inválidos ou incompletos
- Inconsistência nos nomes das colunas
- Mistura de texto e valores numéricos
- Problemas de codificação de caracteres (acentuação)

## Decisões adotadas
- **Registros não foram removidos**, mesmo quando havia campos vazios, para evitar perda de informações relevantes.
- A limpeza foi aplicada **no nível do campo**, e não do registro completo.
- O arquivo CSV original foi mantido como referência, e o tratamento foi realizado em um novo arquivo Excel.

## Tratamentos realizados

### Padronização estrutural
- Renomeação e padronização dos nomes das colunas.
- Ajuste do formato de datas.
- Conversão de valores monetários para formato numérico consistente.
- Correção de problemas de codificação (acentos e caracteres inválidos).

### Correção de valores numéricos
- Identificação e correção de erros de cálculo (`#NÚM!`) no campo `valor_compra`.
- Garantia de que o campo `valor_compra` contenha apenas valores numéricos válidos.

### Tratamento de campos vazios
- Campos vazios foram mantidos quando não era possível inferir o valor correto.
- Foi criada a coluna `dados_completos` para indicar se o registro possui todas as informações preenchidas (`Sim` ou `Não`).

### Tratamento de e-mails
- Identificação de e-mails inválidos, como:
  - Apenas `@`
  - `@com`
  - Endereços sem domínio válido
- A exclusão foi aplicada **somente ao valor do campo de e-mail**, mantendo o restante do registro intacto.
- E-mails válidos foram mantidos sem alteração.

## Estrutura dos arquivos
- `Dados Sujos.csv` → Base original com inconsistências.
- `dados limpos.xlsx` → Base tratada e padronizada, pronta para análise.

## Resultado
A base final está organizada, padronizada e preparada para análises exploratórias, relatórios e visualizações, mantendo a integridade dos dados e refletindo decisões técnicas comuns no trabalho de análise de dados.

## Ferramentas utilizadas
- Microsoft Excel

## Observação
Este projeto tem foco em **limpeza e preparação de dados**, etapa fundamental do processo de análise, simulando problemas reais encontrados em bases utilizadas no dia a dia profissional.
