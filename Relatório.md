<h1>Guess The Number XTREME</h1>

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/873ca457-5cee-4fa4-a0ce-073fbfe3a95e)

Além do protótipo usual do jogo, temos adicionado à interface um botão que mostra a soma
das coordenadas nos valores associados a linguagem do jogo (-8 a 7) e os respectivos
valores em hexadecimal, aleatório e jogo.

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/9af73016-3c01-4dfd-a31d-15aefc2d00b8)

A seguir temos o cronômetro, a lógica é simples, baseia-se num incrementador do tipo
soma, mas advém da subtração 1 a 1 dos valores. Temos diversas entradas associadas.

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/d0e07e30-c03a-4294-bcc3-ced12e85f899)

Essa estrutura analisa as possibilidades para que um cronômetro comece ou pare. No caso
do jogo temos que começar todas as vezes que A ou B está jogando ou quando o
cronômetro do adversário estiver zerado.

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/119701e8-9c8b-4084-a482-cbb513d3c6ac)

Esse circuito desabilita o clock todas vez que estiver zerado.

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/4170251f-a1cb-4d4e-a235-677d9e7e015e)

Esse circuito anterior cronometra as unidades seja minuto ou segundo: 0 a 9

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/a78d6203-c32b-41a5-820a-ddc10b272a13)

Esse fez o mesmo que o anterior só que para as dezenas: 0 a 5

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/405036fb-4993-4a40-b017-9196f35a8988)

Next/Kick funciona de forma simples, ele cria um valor diferente para quando algum dos
dois seja apertado dando prosseguimento ao jogo. Nesse caso o jogo permanece ativo com
ambos os dois cronômetros ligados:
Segue a parte interna do circuito:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/19802586-26d7-434a-b015-c1804eee32d6)

Receive é a parte mais importante do jogo, pois nesse componente o jogo nasce. No
componente temos que habilitar chute, chutar e a limpeza dos respectivos displays para que
outra coordenada ou jogador tenha sua chance de jogar.
Segue a parte interna do componente:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/5dc9ee29-f3c5-4bff-b40d-d0ede4786b56)

Os túneis usados são altamente intuitivos pelos nomes.
Outra possibilidade para o prosseguimento do jogo é quando algum dos cronômetros estiver
zerado dando oportunidade apenas do outro jogador jogar até que ou seu tempo acabe ou o
seu placar chegue a 15

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/d5c73013-6d98-4997-8c5b-a8fdbf87f6be)

Segue os componentes usados por dentro:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/8f1c09a4-e3df-47bb-a53b-f58884f5c734)

É similar ao chute/kick anterior, porém com bits limitados visto que entra em um ciclo finito
unilateral para um único jogador.
Para a comparação da subtração foi necessário um sistema mais complicado visto que não
foi utilizado o complemento de 2 no jogo.
Segue a seguir o sistema e a parte interna dos componentes:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/929f8be2-c58d-4868-a492-53f1b423fd41)

Peça roxa:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/8daad66b-8da1-497b-9dde-43d3c2002a86)

Peça laranja:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/8f2afb79-9af7-43bd-bd47-ba38f6a90e5e)

Cabe ressaltar que as coordenadas foram comparadas em hexadecimal já que é impossível
que o algum valor possa ser repetido:

Peças azuis:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/26707de8-3e5f-4282-9c8e-d23fae5da323)

Peças vermelhas:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/5098b5a7-70fc-47a2-809d-2c806a2c9f91)

Esse componente desfaz o que o display faz para gerar o -8 a 7, ou seja ela pega por
exemplo o -8 = 1111 e torna ele novamente F, usamos-0 para comparar os valores de acertou.

Para o placar a lógica também foi extremamente fácil, temos a seguir:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/2aa17c30-403f-48d0-aaf1-1527041c3fe5)

Sempre que acertar as coordenadas temos 1 ponto, isso pode ocorrer num jogo mútuo ou
unilateral. No mútuo, quando o jogo acabar quem tiver maior pontuação ganha, ou quem
chegar a 15 primeiro. No unilateral o maior valor ganha quando ambos os cronômetros
chegarem a 00:00 ou o único player fizer 15 também.
Peça rosa a seguir:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/18c5a428-c7db-463e-9cb5-da4b9ef6b928)

Peça amarela:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/7f6f48c5-eddf-4697-8022-eb9729a8ca61)

Peça azul:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/133bfa74-1a7d-4890-811b-eedfb58be9fb)

Demais componentes desenvolvidos:
Limitador de chute: (-8 a 7)

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/411d77d7-d493-44bb-978f-b1c05bad4602)

Comparador:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/580f09e0-d02f-4fe8-a80c-4feef8e34a95)

Esse usa a lógica do jogo anterior: Arquivos serão enviados em conjunto:
FlipFlop Pessoal:

![image](https://github.com/ericllacerda/GuessTheNumberXTREME/assets/100648743/a26fad3d-0fc7-4964-af2c-215c01f15e99)







