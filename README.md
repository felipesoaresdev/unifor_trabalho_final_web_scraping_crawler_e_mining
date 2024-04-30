## Leia-me: Análise da Cobertura da Imprensa da Petrobras no Globo (Atualizado)

Este repositório contém dois notebooks Jupyter que realizam web scraping e análise de dados sobre a cobertura da Petrobras no jornal O Globo.

**1. web_scraping_globo_petrobras.ipynb**

Este notebook utiliza o Selenium para fazer o web scraping de artigos do Globo que mencionam a Petrobras. Ele simula o comportamento de um navegador para interagir com a página e extrai informações como título, data de publicação, resumo e link para o artigo completo. Os dados coletados são armazenados em um arquivo Excel na pasta `output`.

**Funcionalidades:**

* Simulação de um navegador para acessar a página do Globo sobre a Petrobras.
* Extração de títulos, datas de publicação, resumos e links de artigos do Globo que mencionam a Petrobras.
* Verificação da data limite para coletar artigos publicados a partir de uma data específica (**ajustável na variável `data_limite`**).
* Armazenamento dos dados coletados em um arquivo Excel (`dados.xlsx`) na pasta `output`.

**Pré-requisitos:**

* Ter o Python instalado com as bibliotecas Selenium, pandas, webdriver_manager e datetime.

**Como executar:**

1. Instale as bibliotecas necessárias (`pip install selenium pandas webdriver-manager datetime`).
2. Execute o notebook `web_scraping_globo_petrobras.ipynb` no Jupyter Notebook.
3. O arquivo Excel com os dados coletados será salvo na pasta `output/dados.xlsx`.

**Observações:**

* O script utiliza o modo headless do Selenium para executar o navegador em segundo plano.
* A data limite para coleta de artigos pode ser ajustada na variável `data_limite`.

**2. trabalho_final_web_mining_e_crawler_scraping.ipynb**

Neste notebook, analisamos os dados coletados anteriormente para encontrar tendências e padrões na cobertura da Petrobras pelo Globo. Utilizamos técnicas para extrair informações importantes dos dados.

**Funcionalidades:**

* **Análise da frequência de notícias por dia:**
    * Agrupa as notícias por dia e conta quantas notícias foram publicadas em cada dia.
    * Identifica os dias com maior e menor número de notícias.
* **Análise da relação entre o preço das ações da Petrobras e a quantidade de notícias:**
    * Obtém os dados históricos do preço das ações da Petrobras (PETR4) do Yahoo Finance.
    * Mescla os dados de notícias com os dados históricos do preço das ações.
    * Calcula a variação percentual do preço das ações em relação ao dia anterior.
    * Identifica os dias com mudanças significativas no preço das ações (acima de um limite definido).
    * Analisa as notícias publicadas nos dias anteriores às mudanças significativas para identificar possíveis fatores que influenciaram o preço das ações.
* **Visualização dos resultados:**
    * Cria um gráfico que mostra o preço de fechamento das ações da Petrobras e a quantidade de notícias por dia.
    * Destaca os pontos de mudança significativa no preço das ações no gráfico.
* **Identificação de notícias relevantes:**
    * Lista as notícias publicadas nos cinco dias anteriores a cada ponto de mudança significativa no preço das ações.
    * Permite a análise manual das notícias para identificar se elas podem ter impactado o preço das ações.

**Pré-requisitos:**

* Ter o Python instalado com as bibliotecas pandas, yfinance, matplotlib, numpy e datetime.
* Ter os dados coletados no notebook `web_scraping_globo_petrobras.ipynb` armazenados em um arquivo Excel (`dados.xlsx`) na pasta `output`.

**Como executar:**

1. Instale as bibliotecas necessárias (`pip install yfinance matplotlib numpy`).
2. Certifique-se de que o arquivo `dados.xlsx` está na pasta `output`.
3. Execute o notebook `trabalho_final_web_mining_e_crawler_scraping.ipynb` no Jupyter Notebook.
4. Analise os resultados e as notícias listadas para identificar possíveis relações entre a cobertura da imprensa e o preço das ações da Petrobras.

**Observações:**

* A análise da relação entre o preço das ações e a quantidade de notícias é exploratória e não fornece conclusões definitivas.
* A identificação de notícias relevantes é subjetiva e depende da análise manual das notícias.
