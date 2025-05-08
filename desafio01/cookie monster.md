#Cookie Monster Secret Recipe
###### Solved by @Yago Martins
> Este é um CTF sobre Web / Exploração Web.
## About the Challenge
Esse desafio consiste em um site que contém uma flag escondida em alguma parte do sistema do site, desafiando o usuário a explorar os fundamentos do site para decifrar a flag.

[![cookie.png](https://i.postimg.cc/R0xgwzvV/cookie.png)](https://postimg.cc/Mnt08Nch)


## Solution
Ao me deslocar para o link do site, após ler o título do desafio: "Cookie Monster...", eu relacionei esta palavra 'cookie' com os 'cookies', que é uma extensão presente em todos os sites do navegador, imaginando ter alguma dica
sobre como solucionar a flag.

Após clicar em qualquer parte da tela com o botão direito, inspecionar, Aplicativo, Cookies, encontrei uma extensão escrita:"secret_recipe". 

[![Cookie-Monster2.png](https://i.postimg.cc/LXbfBzjB/Cookie-Monster2.png)](https://postimg.cc/WF0hsqWh)

Enfim, me deparei com um texto cifrado: "cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0E5NjRBMTM0fQ%3D%3D",no qual interpretei que %3D%3D corresponde a ==, ficando assim em um código cifrado de base 64, que após decifrar me retornou a flag.

>`pic0CTF{c00k1e_m0nster_l0ves_c00kies_A964A134}`
 
