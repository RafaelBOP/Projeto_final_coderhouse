# Pipeline de Dados Sobre SARS-CoV-2 no Brasil

## Projeto Final Python - Coderhouse

Integrantes:
Rafael Marques e Rafael Pinheiro

API utilizado:
https://opendatasus.saude.gov.br/dataset/covid-19-vacinacao

## Visão Geral

Este projeto consiste em um pipeline de dados que coleta informações de uma API do OPENDATASUS. O objetivo é coletar, tratar e analisar os casos e de SARS-CoV-2 no Brasil, permitindo uma fácil integração e manutenção.


## Funcionalidades

    Coleta de Dados: O pipeline é capaz de realizar chamadas à API para obter dados.

    Alerta Sobre o API: O pipeline possui um alerta sobre o status da requisição ao API.

    Transformação de Dados: Os dados obtidos da API foram transformados conforme as necessidades específicas do projeto. 
    Isso inclui limpeza de dados, conversão de formatos, e qualquer outra manipulação necessária.

    Três DataFrames: Um sobre as informações dos pacientes, outro sobre as informações das vacinas e outro sobre as informações das aplicações.

    DataFrames Relacionais: Os três DataFrames são relacionais à partir da coluna id_paciente.


## Instruções

Neste repositório há um ambiente virtual criado contendo as versões de bibliotecas utilizadas durante este projeto.
Caso opte, é possível rodar apenas o requirements.txt para o uso da correta versão.

Clone este repositório para o seu ambiente local:
git clone https://github.com/RafaelBOP/Projeto_final_coderhouse.git

Crie e ative um ambiente virtual:
cd pipeline_API_SUS
python -m pyvenv
source venv/bin/activate

Instale as dependências do projeto:
pip install -r requirements.txt


## Requisitos do Sistema
    Python 3.x
    Pacotes Python necessários (listados no arquivo requirements.txt)
