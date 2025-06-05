
#XOR Properties
###### Resolvido por @Yago Martins
> Este é um CTF que aborda principalmente as relações de cálculo de *XOR*, contendo várias incógnitas e necessitando de suas mudanças de base.
# Sobre o desafio
Este desafio é sobre o cálculo das relações do *XOR* para obtenção da flag, para melhor entendimento, vamos tratar as relações de *XOR* como o símbolo: ⊕, primeiro o desafio oferece as propriedades das operações do *XOR* para resolver o desafio: 

[![001.png](https://i.postimg.cc/0QrdxyTJ/001.png)](https://postimg.cc/wy8sQgT6)

basicamente são as relações dos cálculos do xor e os resultados que ele oferece, isso será utilizado para encontrar incógntas das seguintes relações de chaves e flag:

[![002.png](https://i.postimg.cc/h4kbWgpf/002.png)](https://postimg.cc/RqTnwrrB)

### Materiais para consulta em caso de dúvidas: 

*Oque é um XOR?* (https://www.bosontreinamentos.com.br/seguranca/criptografia-revisao-de-operacoes-logicas-and-or-xor-e-not/?amp=1)

*Oque é um Hexadecimal?* (https://ehgomes.com.br/informatica/entenda-o-hexadecimal-conceito-uso-e-importancia/)

# Solução

Inicialmente, como mostra a imagem, temos o *XOR* da Key 1; 

A Key 2 é obtida através da relação: [Key 1 ⊕ com (Key 1 ⊕ Key 2)]; 

Mas porque? Como já temos a Key 1, após relacionar a Key 1 com o resultado da (Key 1 com a Key 2); sobrará quem? Sim! Somente a Key 2.

Então seguindo esta lógica de "Subtração" a Key 3 é obtida através da relação [Key 2 ⊕ (Key 2 ⊕ Key 3)];

E finalmente para obter a FLAG precisaremos dos resultados das relações das 3 Keys com o resultado da (⊕Flag com Key 1 ⊕ Key 2 ⊕ Key 3);

Como se fosse um sistema de equações, precisamos solucionar as incógnitas para junta-las e no final voltar um resultado; Então vamos para a prática!

## Etapa 1

[![01.png](https://i.postimg.cc/tCbZNgBt/01.png)](https://postimg.cc/XX2YVnSp)

Com o entendimento das relações de Xor, e os resultados que precisam ser encontrador, vamos utilizar apenas as keys destacadas com a seta na imagem para relaciona-las;  

Mas porque não utilizaremos e relação (⊕ Key 1 com ⊕ Key 2) para obter a Key 2? Pois não será necessário, Tendo a Key 1 e o resultado da (Key 2 com a Key 3) vamos  utilizar suas relações para obter as 3 keys de uma vez! 

Para isso utilizaremos a ferramenta online *Xor Calculator*(https://xor.pw/#) com as seguintes configurações: *InputI = base 16* (entrada de dados 1), *InputII = base 16* (entrada de dados 2) e *Output = base 16* para pegar a *XOR* resultante.

[![02.png](https://i.postimg.cc/Rhskhhh5/02.png)](https://postimg.cc/zHhtPJT0)

## Etapa 2

Tendo finalmente a *XOR* das 3 keys, usando a mesma lógica de "Subtração" de XOR, vamos relacionar as nossas Keys com a última relação *XOR* sobrando somente nossa flag;

Então com as seguintes configurações e trocando a base 16 do resultado para base 256 ASCII, conseguimos de forma direta a obtenção  já em seu próprio formato: 

[![03.png](https://i.postimg.cc/FzB6m6Ch/03.png)](https://postimg.cc/sG5m4TRL)

## Etapa 3

Enfim, basta somente copiar e submeter na plataforma para solucionar o desafio.

[![04.png](https://i.postimg.cc/sgSLdwYR/04.png)](https://postimg.cc/CRh7bCrv)



>`crypto{x0r_i5_ass0c1at1v3}`
 
