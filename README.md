# Red or Black
## Descrição
Red or Black é um jogo de cartas jogado por dois agentes, que possuem um baralho de $n$ cartas vermelhas e $n$ cartas pretas. Para fins de notação, usaremos $n=26$. O jogo se baseia nas tentativas dos agentes em acertar a cor da carta do topo do deck, e o jogo continua até que o baralho acabe.
## Estratégias dos agentes
É definido que a pontuação (score) é o número de chutes corretos que o agente conseguiu. Assim, a estratégia de um agente ingênuo (digamos, uma criança pequena, por exemplo), chamado Agente 1, é de chutar aleatóriamente a cor para cada carta. Seu score esperado, trivialmente, será de $26$. <br>
Porém, o agente mais velho, chamado Agente 2, como um bom matemático e ganancioso, sabe que pode contar cartas nesse jogo, e que chutar a cor a qual existem mais cartas restantes pode aumentar a probabilidade de acertar. Assim sua estratégia será exatamente essa, sempre chutará a cor que tiver mais cartas restantes.
## Problema
Qual é o valor esperado, denotado por $S(n)$, para um baralho de 52 cartas do agente velho? E para um baralho simétrico de $2n$ cartas?

## Resultados
Veremos que, para um baralho de $n$ cartas pretas e $n$ cartas vermelhas, o valor esperado do Score é
$$S(n) = n + 0,5(\sqrt{\pi n} -1 ) + O(1/\sqrt{n})$$
Ou seja, para $n$ suficientemente grande, a aproximação é boa. No caso comum $n=26$, é o suficiente para identificar o inteiro de $S(n)$ mais próximo.
Assim, enquanto a criança tem score médio de $26$, o jogador astuto tem score médio de $30$ 😎 (yeah!)