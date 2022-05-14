# ESG_Data_Challenge

Esta é a minha solução para o desafio proposto https://github.com/deepesg/data_challenge

Fiz ela no ambiente do colab então caso queiram testar, favor se atentar ao fato que o arquivo esta em formato de um Jupyter Notebook (ipynb).

Ao meu ver o desafio estava em achar uma maneira de como juntar as contas de forma a somar os valores de suas folhas imediatas. Na minha solução eu percorro os dados 'de trás pra frente' e para cada entrada eu procuro accounts que tenham a entrada como prefixo. Isto por si só não seria o suficiente pois iria somar valores mais de uma vez conforme vamos conferindo as somas de nós mais proximos a raiz. Para evitar de somar mais de uma vez um valor a solução foi encontrar strings com apenas um 'ponto' a mais que a account que estamos calculando. Em outras palavras: 1.1 é sufixo 'imediato' de 1.1.1, mas não é de 1.1.1.001 e confiro isso olhando o numero de pontos na string.

Foram usadas as bibliotecas pandas e numpy pela praticidade de se mexer com datasets e ganho em velocidade quando comparado a python puro.
