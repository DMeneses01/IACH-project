
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

## Etapas para a execução do seu projeto

1. Todo o código encontra-se no ficheiro "recsys_football.ipynb";

2. O código encontra-se divido por partes (como visto em cima) mas pode ser corrido por inteiro;

3. O cálculo da semelhança pode ser feita de duas formas:
    1. Ao correr a secção de  "Calculation of player similarity", será feita todo o cálculo para uso nas recomendações, o que poderá levar algum tempo;
    2. Ao avançar a secção de "Calculation of player similarity" (sem correr), será feita apenas a leitura do ficheiro "engine.pickle" onde se encontram guardadas várias semelhanças já calculadas do dataset atual (apenas funciona após correr uma primeira vez a secção "Calculation of player similarity").

4. Na secção "Input to get Recommendations" será pedido para inserir a liga em que deseja procurar, seguida da equipa e depois o nome do jogador (no caso de jogadores sem clube, deve-se escolher "Free agent" como liga e depois aparecerão os nomes dos jogadores, sendo necessário escolher um deles);

5. Caso se pretenda filtrar as recomendações por pé preferencial, idade, intensidade no ataque e na defesa ou  liga em que o jogador atua, deve-se alterar no código na secção "Get Recommendations". As variáveis a alterar encontram-se declaradas antes de chamar a função getRecommendations, sendo:

    5.1. Idade: "age_default" <br>
         - "All": todas as idades <br>
         - [X, Y]: idades de X a Y <br>
    5.2. Pé preferencial: "foot" <br>
         - "All": ambos <br>
         - "Left": pé esquerdo <br>
         - "Right": pé direito <br>
    5.3. Intensidade no ataque e na defesa: "workrate" <br>
         - "All": tudo <br>
         - "Low/Medium": pelo menos intensidade Low defensiva e Medium atacante <br>
         - "Low/High": pelo menos intensidade Low defensiva e High atacante <br>
         - "Medium/Low": pelo menos intensidade Medium defensiva e Low atacante <br>
         - "Medium/Medium": pelo menos intensidade Medium defensiva e Medium atacante <br>
         - "Medium/High": pelo menos intensidade Medium defensiva e High atacante <br>
         - "High/Low": pelo menos intensidade High defensiva e Low atacante <br>
         - "High/Medium": pelo menos intensidade High defensiva e Medium atacante <br>
         - "High/High": intensidade High defensiva e High atacante <br>
    5.4. Liga em que joga: "league" <br>
         - "All": todas <br>
         - "Y": nome da liga que se pretende <br>

6. Com o jogador escolhido, serão mostradas as recomendações e explicações do resultado.

> **_Nota:_**  Todas as instalações necessárias poderão ser realizadas através da primeira secção.
