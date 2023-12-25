# Pipeline de Dados Sobre Vacinaçaõ de SARS-CoV-2 no Brasil

## Projeto Final Python - Coderhouse

Integrantes:
Rafael Marques e Rafael Pinheiro

API utilizado:
https://opendatasus.saude.gov.br/dataset/covid-19-vacinacao

## Visão Geral

Este projeto consiste em um pipeline de dados que coleta informações de uma API do OPENDATASUS. O objetivo é coletar, tratar e analisar a cobertura vacinal de de SARS-CoV-2 no Brasil, permitindo uma fácil integração e manutenção.


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

## Trechos de código
| Alerta Sobre a Requisição do API |
|:---------------------:|
| ![Alerta sobre a requisição do API](https://github.com/RafaelBOP/Projeto_final_coderhouse/assets/98050820/8bdd6b0e-0505-4e6e-a2a4-f981a0d00d97)|

| Requisição do API |
|:---------------------:|
|![Requisição do API](https://github.com/RafaelBOP/Projeto_final_coderhouse/assets/98050820/2974300d-57a1-476a-a175-0dc690b5adbb)|

| DataFrame de Aplicação das Vacinas, tratados e com colunas renomeadas |
|:---------------------:|
|![DataFrame de Aplicação das Vacinas, tratados e com colunas renomeadas](https://github.com/RafaelBOP/Projeto_final_coderhouse/assets/98050820/24f9fba8-7668-4307-aa01-54dc950d3fe9)|

| Relação Entre os DataFrames de Pacientes e Aplicações |
|:---------------------:|
|![Relação Entre os DataFrames de Pacientes e Aplicações](https://github.com/RafaelBOP/Projeto_final_coderhouse/assets/98050820/df2a75fd-ea9f-4cf8-8379-8dbf7f78e154)|
