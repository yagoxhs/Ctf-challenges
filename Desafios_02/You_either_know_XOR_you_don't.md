
#You either know, XOR you don't
###### Resolvido por @Yago Martins
> Este é um CTF que estimula o desafiante a solucionar várias etapas de um quebra cabeça, utilizando vários metodos de cálculo com XOR e linguagem de programação para encontrar a flag.
# Sobre o desafio

Este desafio disponibiliza um dado hexadecimal para resolução do desafio, você precisa descobrir qual a chave secreta para decriptografar a flag escondida utilizando *XOR* com a seguinte dica: "lembre-se do formato da flag", tendo isso em mente, vamos utilizar durante o procedimento de resolução do desafio.

[![001.png](https://i.postimg.cc/C178ZB8K/001.png)](https://postimg.cc/DJW0HzBV)

### Materiais para consulta em caso de dúvidas: 

*Oque é um XOR?* (https://www.bosontreinamentos.com.br/seguranca/criptografia-revisao-de-operacoes-logicas-and-or-xor-e-not/?amp=1)

*Oque é um Hexadecimal?* (https://ehgomes.com.br/informatica/entenda-o-hexadecimal-conceito-uso-e-importancia/)

*Oque seriam os Bytes?* (https://www.ime.usp.br/~pf/algoritmos/aulas/bytes.html?)

*Sobre a biblioteca pwn tools:* (https://docs.pwntools.com/en/stable/)

# Solução

## Etapa 1

Para resolução deste desafio, utilizaremos a linguagem de programação python. Acesse o site oficial do python e faça download de sua última versão.(https://www.python.org/downloads/)

[![004.png](https://i.postimg.cc/3RhDRJ0w/004.png)](https://postimg.cc/DWCzphgV)

## Etapa 2

Após o download, abra o terminal *PowerShell* (apertando o botão do windows, digitando *PowerShell* e executando como administrador) logo após digite o comando: "*pip install pwn tools*", este comando irá instalar a biblioteca python referência em exploração de binários para resolver o exercício.

[![001.png](https://i.postimg.cc/rwcmxYFh/001.png)](https://postimg.cc/6yjtNcZR)

## Etapa 3

### Iniciaremos o código do nosso programa para resolução deste desafio.

#### Digite os comandos a seguir :

 "*python3*" (para iniciar o terminal python); 

"*from pwn import**" (importa a biblioteca *pwn tools* que você acabou de instalar);

[![01.png](https://i.postimg.cc/4y4St9F2/01.png)](https://postimg.cc/CBt7pz0b)

"*a = "0e0b213f26041e480b26217f27342e175d0e070a3c5b103e2526217f27342e175d0e077e263451150104"*" (isto atribui a váriavel "a" o hexadecimal fornecido pelo desafio);

"*bytes.fromhex(a)*" (extrai os bytes do hexadecimal);

"*b = bytes.fromhex(a)*" (atribui a variável "b" a função de extração dos bytes do hexadecimal);

"*c = b"crypto{*" (utilizando a dica do enunciado, vamos atriburir a variável "c" a inicial da nossa flag que descobriremos posteriormente);

"*print(xor(b,c))*" (este comando imprime os bytes do hexadecimal de "a" em conjunto com o inicio da flag atribuido a variável "c"); 

[![02.png](https://i.postimg.cc/Kc99w4WF/02.png)](https://postimg.cc/0rwdJ5xH)

Após imprimir este comando, podemos identificar no byte imprimido que tem uma parte "legível" escrito: "myXORke+y" que retirado o + --> "myXORkey", Pronto! encontramos a chave secreta escondida.

Com os dados obtidos, basta criar uma váriavel atribuindo a string da nossa chave secreta, execute: "*d = "myXORkey"*"

Em seguida, basta imprimir nossa flag utilizando o comando: "*print(xor(b,d))*" (faz o xor nos bytes contidos no hexadecimal contidos na váriavel "a" em conjunto com a nossa chave contida na váriavel "d"). 

[![03.png](https://i.postimg.cc/hvJVH4JP/03.png)](https://postimg.cc/XBbZ5bcT)

Enfim! ao final das linhas do código, podemos nítidamente encontar nossa flag.



>`crypto{1f_y0u_Kn0w_En0uGH_y0u_Kn0w_1t_4ll}`
 
