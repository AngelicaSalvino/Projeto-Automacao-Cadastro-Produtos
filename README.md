# Automacoes
Projetos de Automação

# PROJETO DE AUTOMAÇÃO DE CADASTRO DE PRODUTOS EM PYTHON
# O MESMO PODE SER REPLICADO PARA VÁRIOS TIPOS DE PROCESSOS REPETITIVOS

# Passos:
# 1º entrar no sistema da empresa;
# 2º Fazer Login
# 3º Importar base de dados
# 4º Cadastrar 1 produto
# 5º Repetir o processo para todos os outros
# Importação das bibliotecas e do arquivo

# Importação das bibliotecas e arquivo de cadastro

import pandas as pd
import time
import pyautogui

tabela = pd.read_csv("C:/PROJETOS/Automacao/produtos.csv")
print(tabela)

# Início da automatização
# Abrindo o windows e digitando 'edge' - utilizarei o microsoft edge para o cadastro destes produtos

pyautogui.PAUSE = 0.3

pyautogui.press("win")
pyautogui.write("edge")
pyautogui.press("enter")

# Entrar no link do Sistema (Programa online) e/ou fazer o passo a passo para logar em sistema interno exemplo SAP
link = "https://dlp.hashtagtreinamentos.com/python/intensivao/login"
pyautogui.write(link)
pyautogui.press("enter")

# Esperar o site carregar
time.sleep(2)

# Fazer login
pyautogui.click(x=439, y=479)
pyautogui.write("angelica.silva@gmail.com")
pyautogui.press("tab")
pyautogui.write("senhateste")
pyautogui.press("tab")
pyautogui.press("enter")

time.sleep(2)

for linha in tabela.index:

    # Cadastrar 1 produto
    pyautogui.click(x=381, y=334)
         
    pyautogui.write(str(tabela.loc[linha, "codigo"]))
    pyautogui.press("tab")
    pyautogui.write(str(tabela.loc[linha, "marca"]))
    pyautogui.press("tab")
    pyautogui.write(str(tabela.loc[linha, "tipo"]))
    pyautogui.press("tab")
    pyautogui.write(str(tabela.loc[linha, "categoria"]))
    pyautogui.press("tab")
    pyautogui.write(str(tabela.loc[linha, "preco_unitario"]))
    pyautogui.press("tab")
    pyautogui.write(str(tabela.loc[linha, "custo"]))
    pyautogui.press("tab")
    
    obs = tabela.loc[linha, "obs"]
    if not pd.isna(obs):
        pyautogui.write(obs)

    # Clicar para enviar o produto cadastrado
    pyautogui.press("tab")
    pyautogui.press("enter")

    pyautogui.scroll(50000)
