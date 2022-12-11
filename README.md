
# Sistema de recomendação para jogadores de futebol
### Projeto IACH - MECD (2022/2023) 

<br/>

## Autores

- Duarte Meneses - 2019216949 - [@DMeneses01](https://github.com/DMeneses01)
- Patricia Costa - 2019213995 - [@patii01](https://github.com/patii01)

<br/>

## Metas

| Meta              | Data                   | Nova data              |
| ----------------- | ---------------------- | ---------------------- |
| Proposta          | 15 de outubro de 2022  |                        |
| Projeto Final     | 5 de dezembro de 2022  | 11 de dezembro de 2022 |
| Defesa Oral       | 14 de dezembro de 2022 |

<br/>

## Índice do código

| Código                           | Traduzido                          | 
| ----------------------           | ----------------------             | 
| Installations                    | Instalações                        |                      
| Imports                          | Imports                            | 
| Read Data                        | Leitura do Dataset                 |
| Basic idea of initial dataset    | Ideia básica do Dataset original   |
| Data treatment                   | Tratamento de dados                |
| Statiscal Analysis               | Análise estatística                |
| Continue preparing data          | Continuação da preparação de dados | 
| Basic idea for final dataset     | Ideia básica do Dataset final      |
| PCA                              | PCA                                |
| Calculation of player similarity | Cálculo da semelhança de jogadores |
| Read pickle                      | Leitura do pickle                  |
| Input to get Recommendations     | Input para as recomendações        |
| Get Recommendations              | Recomendações                      |
| Explanations                     | Explicações                        |

<br/>

## Etapas para a execução do código

1. Todo o código encontra-se no ficheiro "recsys_football.ipynb";

2. Para correr, basta descarregar a pasta code como está no repositório. A estrutura é a necessária para ler os dados;

3. O código encontra-se divido por partes (como visto em cima) mas pode ser corrido por inteiro;

4. O cálculo da semelhança pode ser feita de duas formas:
    1. Ao correr a secção de  "Calculation of player similarity", será feita todo o cálculo para uso nas recomendações, o que poderá levar algum tempo (necessário na primeira vez);

    2. Ao avançar a secção de "Calculation of player similarity" (sem correr), será feita apenas a leitura do ficheiro "engine.pickle" onde se encontram guardadas várias semelhanças já calculadas do dataset atual (apenas funciona após correr uma primeira vez a secção "Calculation of player similarity").

5. Na secção "Input to get Recommendations" será pedido para inserir a liga em que deseja procurar, seguida da equipa e depois o nome do jogador (no caso de jogadores sem clube, deve-se escolher "Free agent" como liga e depois aparecerão os nomes dos jogadores, sendo necessário escolher um deles);

6. Caso se pretenda filtrar as recomendações por pé preferencial, idade, intensidade no ataque e na defesa ou  liga em que o jogador atua, deve-se alterar no código na secção "Get Recommendations". As variáveis a alterar encontram-se declaradas antes de chamar a função "getRecommendations", sendo:

    1. Idade: "age_default" 
         - "All": todas as idades 
         - [X, Y]: idades de X a Y 
    2. Pé preferencial: "foot" 
         - "All": ambos 
         - "Left": pé esquerdo 
         - "Right": pé direito 
    3. Intensidade no ataque e na defesa: "workrate" 
         - "All": tudo 
         - "Low/Medium": pelo menos intensidade Low defensiva e Medium atacante 
         - "Low/High": pelo menos intensidade Low defensiva e High atacante 
         - "Medium/Low": pelo menos intensidade Medium defensiva e Low atacante 
         - "Medium/Medium": pelo menos intensidade Medium defensiva e Medium atacante 
         - "Medium/High": pelo menos intensidade Medium defensiva e High atacante 
         - "High/Low": pelo menos intensidade High defensiva e Low atacante 
         - "High/Medium": pelo menos intensidade High defensiva e Medium atacante 
         - "High/High": intensidade High defensiva e High atacante 
    4. Liga em que joga: "league" 
         - "All": todas 
         - "Y": nome da liga que se pretende 

7. Com o jogador escolhido, serão mostradas as recomendações e explicações do resultado.

> **_Nota 1:_**  Todas as instalações necessárias poderão ser realizadas através da primeira secção.
> **_Nota 2:_**  O código está desenvolvido para fazer recomendações dos primeiros 5772 jogadores (30% do dataset) por uma questão de tempo de execução. Se se pretender executar com todos os jogadores do dataset disponíveis, basta remover do código todas as ocorrências de 5772.
