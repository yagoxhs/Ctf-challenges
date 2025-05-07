#Interencdec
###### Solved by @Yago Martins
> This is a CTF about Reverse Engineering / Script Logic.
## About the Challenge
Esse desafio oferece ao desafiante um arquivo contendo um texto cifrado, no qual ele terá de usar diversos métodos de decifração a partidar da análise dos resultados.
![Cookie Monster Recipe](image/cookie.png)


## Solution
Ao me deslocar para o link do site, após ler o título do desafio: "Cookie Monster...", eu relacionei esta palavra 'cookie' com os 'cookies', que é uma extensão presente em todos os sites do navegador, imaginando ter alguma dica
sobre como solucionar a flag.

Após clicar em qualquer parte da tela com o botão direito, inspecionar, Aplicativo, Cookies, encontrei uma extensão escrita:"secret_recipe". 
![Secret Recipe](image/CookieMonster2.png)

Enfim, me deparei com um texto cifrado: "cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0E5NjRBMTM0fQ%3D%3D",no qual interpretei que %3D%3D corresponde a ==, ficando assim em um código cifrado de base 64, que após decifrar me retornou a flag.

>`pic0CTF{c00k1e_m0nster_l0ves_c00kies_A964A134}`
 

