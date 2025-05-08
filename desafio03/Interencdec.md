#Interencdec
###### Solved by @Yago Martins
> This is a CTF about Reverse Engineering / Script Logic.
## About the Challenge
Esse desafio oferece ao desafiante um arquivo sem extensão, que ao abrir como '.txt' contem um texto codificado, no qual o desafiante terá de usar diversos métodos de decodificação a partir da análise dos resultados.

[![convert-intro.png](https://i.postimg.cc/66dwJBmt/convert-intro.png)](https://postimg.cc/rzF752TP)


## Solution
Ao analisar o texto, você pode deduzir que se trata de uma string codificada com base 64 pelo conjunto de caracteres, tamanho e por terminar com = ou ==.

após decodificar você obtém:

[![convert-passo1.png](https://i.postimg.cc/Cx5W10mZ/convert-passo1.png)](https://postimg.cc/k2rj10r9)

Vemos que se trata de outra string codificada na base 64 por seguir o mesmo padrão, exceto pelos caracteres: (b' ') "indicando" que nossa próxima string a ser decodificada esta entre ' ';

Após decodificar novamente em base 64 obtemos:

[![convert-passo2.png](https://i.postimg.cc/Pr3R0cTd/convert-passo2.png)](https://postimg.cc/Xp5LCsrP)

O resultado que obtemos, ao fazer uma breve análise, percebe-se que está num formato de uma flag pelo padrao de {_ex_ex_} e pelas caracteres aleátorias, pode ter a chance de ser uma string codificada pela Cifra de César, que após decodificar, obtemos a flag.

[![convert-passo3.png](https://i.postimg.cc/pX6ssFJT/convert-passo3.png)](https://postimg.cc/BX256ty9)



>`picoCTF{caesar_d3cr9pt3d_b204adc6}`
 

