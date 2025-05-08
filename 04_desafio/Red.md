#Cookie Monster Secret Recipe
###### Resolvido por @Yago Martins
> Este CTF é sobre Esteganografia.
## Sobre o desafio
O desafio diponibiliza uma imagem '.png' para download: (https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png).

Após o download deverá ser feito uma análise de sua construção para encontrar a flag.

[![Redintro.png](https://i.postimg.cc/Nj5Y9mpk/Redintro.png)](https://postimg.cc/hXWNNzFX)


## Solução
O primeiro passo, é acessar a ferramenta Online "CyberChef" e dar upload da imagem na ferramenta (Extract LSB) para extrair os bits dos dados binários da imagem.

[![Red0.png](https://i.postimg.cc/HLgZDCc8/Red0.png)](https://postimg.cc/w1wcLZk9)

Após isso será preciso configurar as opções de cores "Colour Pattern" para o Cyber Chef extrair os bits da imagem na ordem correta, após identificar nas dicas do desafio, você chega na conclusão que a ordem será: (R G B A) - Red, Green, Blue, Alpha.

[![Redsite.png](https://i.postimg.cc/QtrHJ0z3/Redsite.png)](https://postimg.cc/3yn8KC7S)

Após aplicar as configurações, o site retorna uma codificação de base 64 em loop, no qual é identificado pelo padrão de ordenamento e estrutura das caracteres: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="

[![Red2.png](https://i.postimg.cc/gjxFXPKk/Red2.png)](https://postimg.cc/2LNXMMJP)

Aplicado uma outra ferramenta(From Base 64) em conjunto com o (Extract LSB), Enfim teremos nossa flag completa:

[![Red3.png](https://i.postimg.cc/fTFX0jMw/Red3.png)](https://postimg.cc/mtYhv9cq)

>`picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}`
 
