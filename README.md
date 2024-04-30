
## Web Scraping notícias do G1 sobre Petrobras

Este repositório contém um script Python para coletar dados de notícias sobre a Petrobras do portal G1.

### Pré-requisitos

-   Python 3.x
-   Bibliotecas:
    -   selenium
    -   beautifulsoup4
    -   webdriver_manager
    -   pandas
    -   requests
-   Navegador Google Chrome (necessário para executar o script)

### Instalação das dependências

Você pode instalar as bibliotecas necessárias usando o comando `pip`:

Bash

```
pip install selenium beautifulsoup4 webdriver-manager pandas requests

```

### Como funciona o script

O script utiliza a biblioteca Selenium para abrir o navegador Chrome em modo headless (sem interface gráfica) e acessar a página inicial de notícias sobre a Petrobras no G1. Em seguida, ele percorre a lista de notícias e extrai os seguintes dados de cada uma:

-   Título
-   Link
-   Data de publicação (se disponível)

O script continua carregando novas páginas até encontrar uma notícia publicada antes de uma data limite definida (por padrão, 01/01/2022).

Após coletar os dados, o script cria um DataFrame do Pandas e salva as informações em um arquivo Excel chamado "dados.xlsx".

### Executando o script

1.  Salve o script como um arquivo Python (por exemplo, coletar_noticias_petrobras.py).
2.  Abra um terminal ou prompt de comando e navegue até o diretório onde salvou o script.
3.  Execute o script usando o seguinte comando:

Bash

```
python coletar_noticias_petrobras.py

```

### Arquivo de saída

O script irá gerar um arquivo Excel chamado "dados.xlsx" contendo os dados coletados das notícias sobre a Petrobras.

### Licença

Este script é fornecido como exemplo e pode ser usado ou modificado de acordo com a sua necessidade.
