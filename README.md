# Projeto FINAL - Bootcamp Data Science

Projeto de conclusão elaborado como parte integrante do Bootcamp de Data Science da Alura
---

No presente repositório inserimos o notebook e os dados utilizados na análise realizada para elaboração do PROJETO FINAL do Bootcamp de Data Science Aplicada da Alura. Um maior detalhamento acerca do projeto poderá ser obtido neste resumo e por meio dos links indicados.

---
## 1-Motivação

Conforme exposto no próprio notebook, inicialmente o que nos motiva a realizar este projeto é o próprio desafio proposto no Bootcamp de Data Science da Alura, sendo esta motivação inicial amplificada substancialmente em razão da possibilidde de contribuir com um projeto de cunho prático de um grande hospital. A isso se soma o fato de trabalhar com uma temática que é o foco central da vida de todos atualmente, em âmbito mundial, onde a proposta é a tentativa de melhorar uma previsão que, se bem implementada, poderá contribuir para o salvamento de vidas. Embora nosso conhecimento ainda seja inicial e básico a respeito do assunto "Machine Learning", de maneira especifica, e "Data Science", de maneira geral, certamente tentamos fazer o melhor, embora saibamos que muito há para ser melhorado no projeto e que há outras formas de trabalhar a questão proposta.

---
## 2-Dados

Os dados para este projeto foram obtidos no endereço https://www.kaggle.com/S%C3%ADrio-Libanes/covid19, tendo sido disponibilizados pelo Hospital Sirio Libanes, por meio da plataforma KAGGLE.

![image](https://user-images.githubusercontent.com/82055876/131427160-89a394ef-6de6-45d1-8177-e7adb35c52ce.png)

Com relação a relevância da proposta, o gráfico abaixo ilustra a urgente necessidade de "achatamento da curva", uma das razões para a elaboração e implementação deste projeto, a fim de evitar o colapso do sistema de saúde. Os dados individuais de pacientes, disponibilizados pelo hospital, serão utilizados em detrimento de dados epidemiológicos e populacionais, como normalmente são empregados para avaliações e estimativas acerca da sobrecarga do sistema.

![image](https://user-images.githubusercontent.com/82055876/131425878-52eca3fe-3aa6-4fbf-b6f2-fedd1ea6cab4.png)

Seguem outras informações obtidas acerca do *dataset*, disponibilizadas no site KAGGLE:

Saída: ICU (que significa UTI) é a variável alvo.

Conceito de janela (window): foi tomado o cuidado de incluir cenários da vida real nos eventos e dados disponíveis.

Os dados foram obtidos e agrupados por:

* paciente
- encontro com paciente 
- agregado por janelas em ordem cronológica, conforme segue:

![image](https://user-images.githubusercontent.com/82055876/131428441-2b1cc541-d670-4ad6-afb0-14b3bb0f63ed.png)


* Tomou-se o cuidado para NÃO usar os dados quando a variável alvo estiver presente, pois não se sabe a ordem do evento (talvez o evento-alvo tenha acontecido antes dos resultados serem obtidos). Eles foram mantidos para que possamos expandir este conjunto de dados em outros resultados posteriormente.

Exemplos:

![image](https://user-images.githubusercontent.com/82055876/131426668-e74f7bca-1542-47e4-bd23-5f0b6559ce3c.png)

![image](https://user-images.githubusercontent.com/82055876/131426690-68ad6e61-2b5b-4f87-8e6b-aeac936ed077.png)


### Dataset

Este conjunto de dados contém dados anônimos do Hospital Sírio-Libanês, localizado em São Paulo e Brasília. Todos os dados foram anonimizados seguindo as melhores práticas e recomendações internacionais. Os dados foram limpos e dimensionados por coluna de acordo com Min Max Scaler para caber entre -1 e 1.

### Dados disponíveis

- Informações demográficas do paciente (03)
- Grupo de doenças anteriores do paciente (09)
- Resultados sanguíneos (36)
- Sinais vitais (06)

No total são 54 características, expandidas quando pertinentes à média, mediana, máxima, min, diff e diff relativo.

- diff = max - min
- diff relativo = diff/mediana

---
## 3-Projeto
O objetivo do projeto é, conforme proposto pelo citado hospital, montar uma máquina preditiva com a finalidade de auxiliar na previsão de quais pacientes necessitarão ser encaminhados à unidade de terapia intensiva (UTI) e, dessa forma, contribuir com o manejamento de leitos de UTI do hospital, conforme a necessidade, sendo estas previsões realizadas a partir dos dados clínicos individuais disponíveis de alguns pacientes. É importante mencionar que o anonimato destes pacientes foi garantido pelo hospital.

Basicamente, conforme disponibilizado nas tarefas (tasks) do Kaggle, seria:

* Prever admissão na UTI de casos COVID-19 confirmados;
* Prever NÃO admissão à UTI de casos COVID-19 confirmados.

O presente projeto foi dividido conforme abaixo, a fim de faciliar a análise e testes dos modelos:

* Importação dos dados;
* Análise exploratória dos dados;
* Implementação de modelos de Machine Learning (com dados originais e com dados ajustados);
* Conclusão
* Referências

Importante mencionar que os modelos foram testados de diferentes formas, a partir de técnicas e métodos diversos, com a finalidade de verificar o que apresentasse a melhor acurácia e que proporcionasse maior eficiência. Foi por esse motivo também que, na 2ª Fase do projeto, optamos por eliminar diversas colunas que possuíam alta correlação, abrangendo assim diversas formas de testes, inclusive com a modificação nos dados.

No decorrer do estudo há outras etapas que fizeram parte do projeto, com respectivos comentários acerca das ações tomadas e conclusões obtidas ao longo do notebook, o qual pode ser acessado por meio do link https://github.com/anderboni/Projeto_FINAL_Bootcamp_Data_Science/blob/main/Projeto_FINAL.ipynb

---
## 4-Conclusões

As conclusões que obtivemos a partir da análise dos dados são apresentadas ao final do notebook, entretanto convém advertir que são parciais. Outros estudos posteriores deverão ser realizados para que seja possível aprimorar os modelos e ampliar a eficácia e aplicabilidade dos mesmos.

---
## 5-Continuidade e Considerações Finais

O presente projeto ainda carece de análises mais profundas e mantêm-se em aberto para futuras alterações e aprimoramento.

