#Cookie Monster Secret Recipe
###### Solved by @Yago Martins
> This is a CTF about Binary Exploitation.
## About the Challenge
Esse desafio começa com o desafiante tendo acesso a um arquivo de código fonte '.py' e um link de conexão ncat para rodar um programa: '$ nc verbal-sleep.picoctf.net 60492' o programa roda versos de uma música que ao final de sua primeira parte de execução pede o input de uma senha 'Crowd' para decidir como o programa irá funcionar. O desafio conciste basicamente em você analisar o código fonte para saber qual 'Crowd' correta para o programa lhe retornar uma flag entre os versos da música.
![primeira parte flag](imagens/primeiraparte.png)

## Solution
O primeiro passo a se fazer é abrir o código fonte e analisá-lo, logo nas primeiras linhas do código, você já identifica a posição da flag, como mostra a imagem:
![segunda parte flag](imagens/primeiraparte.png)


>`pic0CTF{c00k1e_m0nster_l0ves_c00kies_A964A134}`
 
