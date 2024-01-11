# Pipeline de Dados Sobre Vacinação de SARS-CoV-2 no Brasil

## Índice
- [Visão Geral](#visão-geral)
- [Funcionalidades](#funcionalidades)
- [Intruções](#intruções)
- [Requisitos do Sistema](#requisitos_do_sistema)
- [Informações sobre o Pipeline](#informações_sobre_o_pipeline)
- [Exemplos do Código](#exemplos_do_código)
- [Autores](#autores)
- [Referências](#referêcias)


## Visão Geral

Este projeto consiste em um pipeline de dados que coleta informações de uma API do OPENDATASUS. O objetivo é coletar, tratar e analisar  dados sobre a cobertura vacinal de de SARS-CoV-2 no Brasil, permitindo uma fácil integração e manutenção.


## Funcionalidades

    Coleta de Dados: O pipeline é capaz de realizar chamadas à API para obter dados.

    Alerta Sobre o API: O pipeline possui um alerta sobre o status da requisição ao API.

    Transformação de Dados: Os dados obtidos da API foram transformados conforme as necessidades específicas do projeto. 
    Isso inclui limpeza de dados, conversão de formatos, e qualquer outra manipulação necessária.

    Três DataFrames: Um sobre as informações dos pacientes, outro sobre as informações das vacinas e outro sobre as informações das aplicações.

    DataFrames Relacionais: Os três DataFrames são relacionais à partir da coluna id_paciente.


## Instruções

Neste repositório há um ambiente virtual criado contendo as versões de bibliotecas utilizadas durante este projeto.
Caso opte, é possível utilizar o requirements.txt para o uso das versões corretas.


## Requisitos do Sistema
    Python 3.x.
    Bibliotecas do Python necessárias e com o versionamento listados em requirements.txt.

## Informações sobre o Pipeline

1. Requisição do API

A API será requisitada e será retornado um aviso através da função alerta_API sobre o status da requisição.

2. Manipulação inicial

Os dados JSON obtidos pela API devem ser normalizados para a criação dos DataFrames.
Foram criados três DataFrames cuja coluna de relaciomente escolhida entre os três é a _id (no projeto com o alias de id_paciente)
As informações originais foram divididas em DataFrames dos pacientes, outro para as informações das vacinas e por fim um DataFrame contendo as informações sobre as aplicações das vacinas.   

|DataFrame sobre os pacientes|
|:---------------------:|
As colunas utilizadas são: 
- id_paciente
- data_nascimento
- idade	
- codigo_raca
- sexo
- UF
- codigo_municipio
  
|DataFrame sobre as vacinas|
|:---------------------:|
As colunas utilizadas são: 
- id_paciente
- nome_vacina
- fabricante
- lote
- lote_vacina
- codigo_categoria
- grupo_atendimento
- status

|DataFrame sobre as aplicações|
|:---------------------:|
As colunas utilizadas são:
- id_paciente
- nome_vacina
- categoria_aplicacao
- UF_estabelecimento
- nome_municipio
- razao_social
- data_aplicacao
- descricao_dose
- numero_dose


3. Tratamento dos DataFrames

Os DataFrames tiveram suas colunas renomeadas para sua melhor compreensão.
As colunas que estavam com seu tipo errado também foram ajustados para o correto.
Por fim, foi verificada a existência de dados nulos. As linhas nulos foram excluídas.

4. Relacionamento dos DataFrames

Os três DataFrames possuem um relacionamente através da coluna id_paciente. 
Um left join foi realizado sempre priorizando as informações desejadas no DataFrame esquerdo.

5. Resultado

Ao final, foram gerados três novos DataFrames:
- Informações da aplicação por paciente
- Informações da vacina por paciente.
- Informações da vacina por aplicação.

## Exemplos do Código
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

## Autores
Rafael Marques e Rafael Pinheiro

## Referências
[API utilizado](https://opendatasus.saude.gov.br/dataset/covid-19-vacinacao)
