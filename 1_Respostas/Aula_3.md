

Para todas as questões, compile-as com o gcc e execute-as via terminal.

    1.
    
```C    
      #include <stdio.h>
      #include <stdlib.h>


      int main(int argc, char **argv)
      {

        printf("Ola mundo !! \n");
        return 0;
      }
```      

    2.
```C
      #include <stdio.h>
      #include <stdlib.h>


      int main(int argc, char **argv)
      {
        char str [80];
        printf("Digite o seu nome: ");
        scanf("%s",str);

        printf("Ola %s \n",str);
        return 0;
      }
```

    3.Apresente os comportamentos do código anterior nos seguintes casos:
    

(a) 

R: Ele só Imprime Ola Eu. 

(b)

R: Ele só Imprime Ola "Eu.

(c) 

R:Digite o seu nome: Ola Eu 

(d) 

R: Digite o seu nome: Ola Eu.

(e) 

R:Aparece "Digite o seu nome: Ola Eu" 

(f) 

R:aparece "Digite o seu nome: Ola Ola" 

    4.

```C
#include <stdio.h>
#include <stdlib.h>


int main(int argc, char **argv)
{


printf("Ola %s \n",argv[1]);
return 0;
}

```

    5.Apresente os comportamentos do código anterior nos seguintes casos:

(a)

    R: Ele só irá imprimir o primeiro nome no caso : Ola Eu
    

(b) 

    R: Ele irá imprimir os dois nomes : Ola Eu mesmo

(c) 

    R:Ele irá imprimir: Ola (null), pois não há argumento para a variavel argv. 


(d)

    R:Ele irá imprimir: Ola (null), pois não há argumento para a variavel argv. 

(e) 

    R:Ele irá imprimir: Ola (null), pois não há argumento para a variavel argv.     

(f) 

    R:Ele irá imprimir: Ola (null), pois não há argumento para a variavel argv. 

    6.
```C
#include <stdio.h>
#include <stdlib.h>


int main(int argc, char **argv)
{
	int i;
	int x;


	printf("Ola %s \n",argv[1]);

	printf("Número de entradas = %d \n",argc);

return 0;
}

```

    7.Crie um código em C que imprime todos os argumentos de entrada fornecidos pelo usuário. Por exemplo, considerando que o código criado recebeu o nome de 'ola_argumentos':

$ ./ola_argumentos Eu Mesmo e Minha Pessoa
$ Argumentos: Eu Mesmo e Minha Pessoa

    8.Crie uma função que retorna a quantidade de caracteres em uma string, usando o seguinte protótipo: int Num_Caracs(char *string); Salve-a em um arquivo separado chamado 'num_caracs.c'. Salve o protótipo em um arquivo chamado 'num_caracs.h'. Compile 'num_caracs.c' para gerar o objeto 'num_caracs.o'.

    Re-utilize o objeto criado na questão 8 para criar um código que imprime cada argumento de entrada e a quantidade de caracteres de cada um desses argumentos. Por exemplo, considerando que o código criado recebeu o nome de 'ola_num_caracs_1':

$ ./ola_num_caracs_1 Eu Mesmo
$ Argumento: ./ola_num_caracs_1 / Numero de caracteres: 18
$ Argumento: Eu / Numero de caracteres: 2
$ Argumento: Mesmo / Numero de caracteres: 5

    9.Crie um Makefile para a questão anterior.

    Re-utilize o objeto criado na questão 8 para criar um código que imprime o total de caracteres nos argumentos de entrada. Por exemplo, considerando que o código criado recebeu o nome de 'ola_num_caracs_2':

$ ./ola_num_caracs_2 Eu Mesmo
$ Total de caracteres de entrada: 25

    10.Crie um Makefile para a questão anterior.

