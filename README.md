<h1 align="center">Inferência Estatística</h1>



A inferência estatística é um ramo da estatística que se dedica a tirar conclusões sobre uma população a partir de uma amostra. Em outras palavras, é o processo de usar os dados coletados de uma amostra menor para fazer generalizações ou previsões sobre uma população maior.

<br>

O desafio proposto trata sobre o transtorno depressivo, um problema multifatorial que pode ter várias possíveis combinações de situações como causa.

<br>

Os dados disponíveis são resultados da NHNES (National Health and Nutrition Examination Survey), realizada anualmente nos EUA para avaliar a saúde e nutrição de adultos e crianças;

<br>

Perguntas:
    
- Há associação entre gênero e depressão?

- As médias de idade são as mesmas para os três grupos de depressão?

- As médias de renda familiar são as mesmas para os três grupos de depressão?

## Banco de Dados

DEMO_PHQ.csv: banco de dados contendo 5334 observações de adultos pesquisados no NHANES 2005-2006

PAG_HEI.csv: banco de dados contendo 9424 observações de crianças e adultos pesquisados no NHANES 2005-2006

#

Conclusões:

Através de testes de hipoteses que são procedimentos estatístico fundamental usado para determinar se há evidências suficientes em uma amostra de dados para inferir que uma determinada condição é verdadeira para toda a população. Basicamente, é uma maneira de testar se os resultados de um estudo ou experimento são significativos ou se ocorreram por acaso, podemos responder as perguntas !

1. Há associação entre gênero e depressão?


![download](https://github.com/Felintox/Tera_Desafio_Inferencia/assets/129033082/ec2d525f-8bc3-4e46-9c91-e22f45c1d551)

Neste caso queremos comparar as proporções (prevalências) de sintomas de depressão entre os gêneros.<br>Como queremos avaliar a associação entre duas variáveis categóricas, usaremos o teste qui-quadrado.

As hipóteses desse teste serão:

H0 (nula) = Não há associação entre gênero e sintomas de depressão. -> p > 0,05 <br>
H1 (alternativa) = Há associação entre gênero e sintomas de depressão. -> p < 0,05

tivemos um resultado de :

stat = 36.978, p = 0.000

Um valor de p < 0.001, ou seja ha associação entre genero e depressao

o que da para verificar pelo dados que existem um quantidade maiores de pessoas do sexo feminino com sintomas depressivos

2. As médias de idade são as mesmas para os três grupos de depressão?

![download](https://github.com/Felintox/Tera_Desafio_Inferencia/assets/129033082/be16e4af-2706-4988-baf2-598dfb57aefe)

Teste de Hipótese do tipo ANOVA, comparação de media entre mais de 2 variaveis (três grupos)

H0 (nula) = Não existe diferença entre os grupos de depressão com relação à média de idade. -> p > 0,05

H1 (alternativa) = Existe pelo menos uma diferença na média de idade entre os grupos de sintomas de depressão. -> p < 0,05

stat=2.329, p=0.097

Sendo assim, não conseguimos detectar uma diferença estatisticamente significativa entre os grupos de depressão com relação à media de idade.


3. As médias de renda familiar são as mesmas para os três grupos de depressão?

![download](https://github.com/Felintox/Tera_Desafio_Inferencia/assets/129033082/dce9a5e1-d2c4-48d0-86d2-5fcf3f0cc67d)

As hipóteses desse teste serão:

H0 (nula) = Não existe diferença entre os grupos de depressão com relação à média de renda familiar.

H1 (alternativa) = Existe pelo menos uma diferença na média de renda familiar entre os grupos de sintomas de depressão.

stat=49.160, p=0.000

![image](https://github.com/Felintox/Tera_Desafio_Inferencia/assets/129033082/c5b80359-15ee-48cd-95fc-e2d02bfa8db5)

##### Com as comparações múltiplas, estamos realizando três testes de hipótese simultaneamente. Por conta disso, a função ajusta o valor-p para que o erro máximo desde conjunto de teste de hipóteses seja no máximo alpha = 0.05.

##### Teste 1: Grupo 0 (Sem sintomas) x Grupo 1 (sintomas leves) -> p = 0.001

##### Teste 2: Grupo 0 (Sem sintomas) x Grupo 2 (sintomas moderados-severos) -> p = 0.001

##### Teste 3: Grupo 1 (sintomas leves) x Grupo 2 (sintomas moderados-severos) -> p = 0.001

##### Neste caso, rejeitamos todas as hipóteses nulas. Sendo assim, temos indícios de que:

##### A renda média do grupo Sem sintomas é diferente da renda média do grupo de sintomas leves
##### A renda média do grupo Sem sintomas é diferente da renda média do grupo de sintomas moderados-severos
##### A renda média do grupo sintomas leves é diferente da renda média do grupo sintomas moderados-severos
