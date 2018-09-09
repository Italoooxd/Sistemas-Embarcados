

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

    7.

```C
#include <stdio.h>
#include <stdlib.h>


int main(int argc, char **argv)
{
	int x = 1;

	printf("Argumentos: ");
	
	while (x < argc){
	printf("%s ", argv[x]);
	x++;
	}
	printf ("\n");
return 0;
}

```
    8.
    
```C
//num_caracs.c

#include "num_caracs.h"

int Num_Caracs(char *string){
	
	int i = 0;
	
	while(string[i] != '\0'){
		i++;
		
	} 
	return i;

}

```
```C
//numcaracs.h

int num_caracs (char *string);

```
    Re-utilize o objeto criado na questão 8 para criar um código que imprime cada argumento de entrada e a quantidade de caracteres de cada um desses argumentos. Por exemplo, considerando que o código criado recebeu o nome de 'ola_num_caracs_1':

```C
#include <stdio.h>
#include <stdlib.h>
#include "num_caracs.h"


int main(int argc, char **argv)
{
	int x = 0;
	int carac ;
	
	while (x < argc){
	
	carac = num_caracs(argv[x]);		
	printf("Argumentos: %s / Numero de caracteres: %d \n", argv[x], carac);
	x++;
	}
	printf ("\n");
return 0;
}

```

    9.Crie um Makefile para a questão anterior.

num_caracs: aula.o num_caracs.o
	gcc $(CFLAGS) -o num_caracs aula.o num_caracs.o
aula.o: aula.c num_caracs.h
	gcc $(CFLAGS) -c aula.c
num_caracs.o: num_caracs.c num_caracs.h
	gcc $(CFLAGS) -c num_caracs.c
clean:

	rm -f *.o num_caracs


    Re-utilize o objeto criado na questão 8 para criar um código que imprime o total de caracteres nos argumentos de entrada. Por exemplo, considerando que o código criado recebeu o nome de 'ola_num_caracs_2':
```C
#include <stdio.h>
#include <stdlib.h>
#include "num_caracs.h"


int main(int argc, char **argv)
{
	int x = 0;
	int carac ;
	
	while (x < argc){
	
	carac = carac + num_caracs(argv[x]);		
	
	x++;
	}
	printf("Total de caracteres de entrada: %d \n", carac);

return 0;
}

```
    
    10.Crie um Makefile para a questão anterior.

