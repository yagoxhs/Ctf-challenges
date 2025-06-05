
#Favourite Byte
###### Resolvido por @Yago Martins
> Este é um CTF sobre como utilizar *XOR* em linguagem de programação afim de transitar entre os bytes contidos nos dados hexadecimais fornecidos.
# Sobre o desafio

Este desafio começa com a plataforma disponibilizando um dado hexadecimal para resolução do desafio, basicamente o desafio conciste em você achar o *byte* secreto escondindo no dado hexadecimal e fazer seu cálculo utilizando *XOR* e encontrando a flag escondida entre os resultados obtidos.

[![003.png](https://i.postimg.cc/0NbVfnVS/003.png)](https://postimg.cc/Y4BN26K2)


# Solução

## Etapa 1

Para resolução deste desafio, utilizaremos a linguagem de programação python. Primeiro você deverá acessar o site oficial do python e fazer o download de sua última versão.(https://www.python.org/downloads/)

[![004.png](https://i.postimg.cc/3RhDRJ0w/004.png)](https://postimg.cc/DWCzphgV)

## Etapa 2

Após o download, abra o terminal *PowerShell* (apertando o botão do windows, digitando *PowerShell* e executando como administrador) logo após digite o comando: "*pip install pwn tools*", este comando irá instalar a biblioteca python referência em exploração de binários para resolver o exercício.

[![001.png](https://i.postimg.cc/rwcmxYFh/001.png)](https://postimg.cc/6yjtNcZR)

## Etapa 3

### Logo após começaremos a codar nosso programa.

#### Digite os comandos a seguir : 

"*python3*" (para iniciar o terminal python); 

"*from pwn import**" (importa a biblioteca *pwn tools* que você acabou de instalar);

"*a = "73626960647f6b206821204f21254f7d694f7624662065622127234f726927756d"*" (isto atribui a váriavel "a" o hexadecimal desejado);

"*bytes.fromhex(a)*" (extrai os bytes do hexadecimal);

"*b = bytes.fromhex(a)*" (atribui a variável "b" a função de extração dos bytes do hexadecimal);

"*for i in range (0,99):*"(faz um loop de repetição de 0 a 99 para para o xor transitar entre os bytes selecionados);

"*print(xor(b,i)) e pressionar *Enter* duas vezes*" (faz o xor durante o laço de repetição, imprimindo no terminal os resultados obtidos após a relação do xor com cada byte extraído do hexadecimal). 

[![002.png](https://i.postimg.cc/ZK0zWGNP/002.png)](https://postimg.cc/Tp84SHCh)

Após seguir todos estes passos, como visto na imagem, encontraremos nossa flag na posição 17 do loop de repetição!

>`crypto{0x10_15_my_f4v0ur173_by7e}`
 
