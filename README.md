# ClearBank - Análise Financeira com Python

## Descrição do Projeto
Projeto desenvolvido como desafio prático da pós-graduação da Rocketseat para o processamento e validação de dados financeiros da fintech ClearBank. O notebook realiza a ingestão de um arquivo CSV de transações bancárias, aplica tratamento de exceções e regras de validação silenciosa, agrega indicadores financeiros mensais, identifica movimentações de risco/suspeitas e exporta os dados estruturados.

## Tecnologias Utilizadas
* Python 3.10+
* Módulos nativos: `csv`, `json`, `datetime`
* Bibliotecas adicionais: `pandas`, `matplotlib`

## Estrutura dos Arquivos
* `desafio-final.ipynb`: Notebook com o pipeline completo, funções modulares e células executadas.
* `transacoes.csv`: Base de dados contendo registros de crédito e débito com dados válidos e inconsistentes para testes.
* `relatorio.json`: Arquivo gerado automaticamente contendo o consolidado mensal e as transações suspeitas.
* `grafico.png`: Visualização gráfica do saldo mensal gerada via Matplotlib.

## Como Executar
1. Acesse o ambiente do [Google Colab](https://colab.research.google.com/) ou utilize o Jupyter Notebook local.
2. Faça o upload do arquivo `desafio-final.ipynb` e garanta que o arquivo `transacoes.csv` esteja presente no mesmo diretório de execução.
3. Execute todas as células em ordem sequencial:
   * No Google Colab: menu **Ambiente de execução** → **Executar tudo** (ou utilize o atalho `Ctrl + F9`).

## Saídas Geradas pelo Notebook
Ao executar o notebook até o fim, são geradas as seguintes saídas:
1. **Relatório Estruturado no Terminal:**
   * Resumo da limpeza com contadores de linhas lidas, válidas e inválidas.
   * Período analisado e quantidade total de dias decorridos.
   * Agrupamento mensal com total de operações, receitas (`credito`), despesas (`debito`), saldo líquido, média por transação e valores extremos (mínimo e máximo).
   * Listagem de transações suspeitas com valores superiores a R$ 10.000,00.
2. **Arquivo `relatorio.json`:** Arquivo JSON formatado com os dados consolidados do processamento
