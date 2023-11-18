# Projeto de automação de cadastro de produtos em Python

Este projeto automatiza o processo de cadastro de produtos em um sistema de gestão empresarial. O projeto pode ser replicado para diversos tipos de processos repetitivos.

## Passos

1. Entrar no sistema da empresa
2. Fazer login
3. Importar base de dados
4. Cadastrar 1 produto
5. Repetir o processo para todos os outros

## Importação das bibliotecas e do arquivo

O projeto utiliza as seguintes bibliotecas:

* Pandas: para trabalhar com arquivos CSV
* Time: para controlar o tempo de espera entre as ações
* Pyautogui: para controlar o mouse e o teclado

O arquivo de cadastro é um arquivo CSV com os seguintes campos:

* Código
* Marca
* Tipo
* Categoria
* Preço unitário
* Custo
* Observações

## Início da automação

O início da automação consiste em abrir o navegador Microsoft Edge e acessar o link do sistema da empresa. Em seguida, o usuário deve fazer login no sistema.

## Cadastramento de um produto

Para cadastrar um produto, o projeto realiza as seguintes ações:

* Clicar no botão "Novo produto"
* Preencher os campos do formulário de cadastro com as informações do produto
* Clicar no botão "Salvar"

## Repetição do processo

O processo de cadastramento de um produto é repetido para todos os produtos da base de dados.

## Resultado

Ao final da automação, todos os produtos da base de dados serão cadastrados no sistema da empresa.

## Melhorias

O projeto pode ser melhorado de diversas formas, como:

* Adicionando um tratamento de erros para lidar com situações inesperadas, como campos obrigatórios não preenchidos
* Aumentando a velocidade da automação, por exemplo, utilizando a biblioteca Selenium para controlar o navegador
* Adaptando o projeto para outros sistemas de gestão empresarial

## Critérios de aceitação

O projeto deve ser capaz de cadastrar todos os produtos da base de dados sem erros.

