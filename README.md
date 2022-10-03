# Aplicacoes-WebScraping

Trabalho realizado para a disciplina de Coleta, Preparação e Análise de Dados - 4° Semestre da PUCRS pelo curso de Ciência de Dados e Inteligência Artificial

Autores: João Pedro de Moura Medeiros e Andressa Moreira

# Resumo 

O trabalho foi realizado em cima do enunciado disponibilizado pelo professor Lucas da disciplina de CPA. Em vista, na primeira tarefa deve-se fazer determinada raspagem de dados em um ambiente controlado, sendo um freamwork executável como ambiente, tendo páginas com vários países e seus dados. Já na segunda questão é indicado fazer a raspagem de dados em um ambiente real, sendo o ambiente site do IMDB, coletando dados dos 250 melhores filmes.

As tarefas e arquivos estão em formato zip fixados no repositório.

# Web Scraping em ambiente controlado

Como dito, na tarefa 1 foi necessário fazer scraping de um ambiente controlado e pegar os dados de todos os países contidos.

## Executando o ambiente

Obs: é necessário ter o python 2.7 na máquina 

1. Abra o prompt de comando.
2. Entre na pasta aplicacao_testes_scraping.
3. Entre no ambiente conda pelo comando >conda activate webscrap.
4. Entre na pasta web2py27.
5. Execute o comando >python web2py.py, irá abrir uma janela.
6. Nessa janela insira uma senha que se lembre, pode ser simples como 123.
7. Clique na aba meus sites e insira a senha da etapa 6.
8. Clicando em meus places, abrirá uma aba com certos países, seguindo de outros países ao clicar em next.
9. A partir dai basta apenas coletar os dados.

## Coletando os dados

1. As bibliotecas BeautifulSoup, request, time, rs, pandas, numpy e hashlib foram utilizadas no programa.
2. O arquivo tarefa1.ipynb faz um crawler que navega pelas páginas de países. 
3. O arquivo tarefa1 baixa os HTMLs, salvando-os. 
4. O arquivo tarefa1 faz scraping dos HTMLs baixados e os dados retirados são salvos no csv chamado tarefa1.csv
5. O arquivo tarefa1 salva uma coluna extra no csv contendo o timestamp do momento no qual os dados foram obtidos. 
6. O arquivo tarefa1 faz um crawler que monitora as páginas de países através de um While True procurando por atualizações. Atualizando o csv tarefa1.csv quando alguma    mudança ocorre. 
7. Para executar o programa você deve utilizar o comando "Run All" do jupyter notebook.
8. Na última célula do programa existe um While True, esse laço fica eternamente verificando se existem alterações na página, para parar o programa você deve              interromper essa célula.

# Web Scraping em ambiente real

A tarefa 2 foi necessário fazer scraping de um ambiente real, pegando determinados dados pedidos no enunciado dos 250 melhores filmes classificados pela IMDB.

## Coletando os dados

1. Deve-se baixar o chromedriver em seu computador para rodar o ScrapIMBD.
2. Verifique se o seu navegador é da mesma versão que o executável chromedriver.
3. As bibliotecas selenium, request, shutil, os, json e re foram utilizadas no programa.
4. O arquivo ScrapIMBD.ipynb coleta os dados dos 250 melhores filmes da página da IMBD.
5. O arquvio ScrapIMBD.ipynb baixa todos os posters na pasta img_posters.
6. O arquivo ScrapIMBD.ipynb escreve para um arquivo json todos os dados coletados.
7. As categorias dos dados coletados são respectivamente Título, Ano de lançamento url do poster, imagem do poster, nota imdb, lista de gêneros e lista de diretores.
