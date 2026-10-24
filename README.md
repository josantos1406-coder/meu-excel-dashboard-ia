# Painel de clientes

Painel em um único arquivo HTML que mostra estatísticas e gráficos de valores e datas, importa planilhas do Excel e salva o resultado em CSV, PDF e Word.

## Como usar

1. Salve o arquivo `painel_clientes_download.html` no computador.
2. Abra com um duplo clique no navegador (precisa de internet, veja Requisitos).
3. Clique em **Importar Excel** e escolha sua planilha. Sem importar nada, o painel mostra 15 clientes de exemplo.
4. Use **Salvar em CSV**, **Salvar em PDF** ou **Salvar em Word** para baixar os dados.

## Formato da planilha

A primeira linha precisa ter estes títulos de coluna. Maiúsculas e acentos não importam.

| Coluna  | Conteúdo                                      | Exemplo                |
|---------|-----------------------------------------------|------------------------|
| ID      | Identificador do cliente                      | 1                      |
| Nome    | Nome do cliente (também aceita `Cliente`)     | Ana Souza              |
| Produto | Produto comprado                              | Notebook Dell Inspiron |
| Valor   | Número ou texto como `R$ 1.234,56`            | 4299,90                |
| Data    | Data em `dd/mm/aaaa` ou `aaaa-mm-dd`          | 03/09/2026             |

Formatos aceitos: `.xlsx`, `.xls` e `.csv`. Só a primeira aba da planilha é lida. Linhas sem nome, valor ou data válidos são ignoradas. Os dados importados substituem os que estavam na tela.

## O que o painel mostra

- **Estatísticas:** número de registros, valor total, valor médio, mediana, maior e menor valor (com o nome do cliente), período das datas e mês de maior valor.
- **Gráficos:**
  - maiores valores por cliente (até 15);
  - valor acumulado ao longo das datas;
  - quantidade de clientes por faixa de preço (5 faixas entre o menor e o maior valor).
- **Tabela** com todos os registros.

## O que cada exportação contém

| Formato | Conteúdo                                              |
|---------|-------------------------------------------------------|
| CSV     | Tabela completa, separada por `;`, pronta para abrir no Excel em português |
| PDF     | Estatísticas, os três gráficos e a tabela             |
| Word    | Estatísticas e a tabela (sem gráficos)                |

## Requisitos

- Um navegador atual (Chrome, Edge, Firefox ou Safari).
- Conexão com a internet na hora de abrir, para carregar as bibliotecas Chart.js, SheetJS, jsPDF e JSZip e a fonte Schibsted Grotesk. Se a fonte não carregar, o painel usa a fonte padrão do sistema.

## Observações

- Nada é enviado a servidores: a leitura da planilha e a geração dos arquivos acontecem no seu navegador.
- Os dados não ficam guardados. Ao fechar ou recarregar a página, volta para os dados de exemplo.
- O tema claro ou escuro segue a configuração do seu sistema.

## Arquivos

- `painel_clientes_download.html`: versão para baixar e abrir no computador.
- `tabela_clientes.xlsx`: planilha de exemplo com os 15 clientes, já no formato certo para importar.
