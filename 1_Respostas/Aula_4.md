

Para todas as questões, utilize as funções da biblioteca stdio.h de leitura e de escrita em arquivo (fopen(), fclose(), fwrite(), fread(), dentre outras). Compile os códigos com o gcc e execute-os via terminal.

    1.
    
```C
#include <stdio.h>
#include <stdlib.h>

int main(int argc, const char * argv[]) {
  FILE *fp;
  char string[100] = "Ola mundo !!";
  int i;
  fp = fopen("ola_mundo.txt","w");
  
  	fputs(string, fp);                                         
  	putc('\n', fp);
  	fclose(fp);
  return 0;
}
```
    2.
```C
#include <stdio.h>
#include <stdlib.h>

int main(int argc, const char * argv[]) {
  FILE *fp;
  char nome[100] ;
  int idade;

  fp = fopen("ola_mundo.txt","w");

 	printf("Digite seu nome: ");
 	scanf("%s", nome);
 	printf("Digite sua idade: ");
 	scanf("%i", &idade); 
 	fprintf(fp, "Nome: %s\n", nome);
 	fprintf(fp, "Idade: %i\n", idade);
  	fclose(fp);
  return 0;
}

```

    3.
```C

#include <stdio.h>
#include <stdlib.h>

int main(int argc, const char * argv[]) {
  FILE *fp;
  char nome[100] ;
  int idade;

  fp = fopen("ola_mundo_2.txt","w");

 	fprintf(fp, "Nome: %s\n", argv[1]);
 	fprintf(fp, "Idade: %s\n", argv[2]);
  	fclose(fp);
  return 0;
}

```
  
    4.
```C
//bib_arqs.c
#include "bib_arqs.h"
#include <stdio.h>
#include <stdlib.h>


int tam_arq_texto(char *nome_arquivo) {
  FILE *fp;
  
  int i=0;
  char c;
  fp = fopen(nome_arquivo,"r");
  c = getc(fp);
  while (!feof(fp))        
    {
    	i++;
      	c = getc(fp);   
    }
    printf("Seu arquivo tem %i bytes\n",i);
	fclose(fp);
  return 0;
}

```
```C
//bib_arqs.h

int tam_arq_texto(char *nome_arquivo);

```
    5.
```C
#include "bib_arqs.h"
#include "le_arq_texto.h"
#include <stdio.h>
#include <stdlib.h>


int tam_arq_texto(char *nome_arquivo) {
  FILE *fp;
  
  int i=0;
  char c;
  fp = fopen(nome_arquivo,"r");
  c = getc(fp);
  while (!feof(fp))        
    {
    	i++;
      	c = getc(fp);   
    }
    printf("Seu arquivo tem %i bytes\n",i);
	fclose(fp);
  return 0;
}

char* le_arq_texto(char *nome_arquivo){
	FILE *p;
	char arquivo[1000];
	char c;
	int i;
	p = fopen(nome_arquivo,"r");
    c = getc(p);
    while (!feof(p))    
    {
        
        arquivo[i] = c; 
        c = getc(p);
        i++;    
    }
    fclose(p);         


}

```
    6.Crie um código em C que copia a funcionalidade básica do comando cat: escrever o conteúdo de um arquivo-texto no terminal. Reaproveite as funções já criadas nas questões anteriores. Por exemplo, considerando que o código criado recebeu o nome de 'cat_falsificado':

$ echo Ola mundo cruel! Ola universo ingrato! > ola.txt
$ ./cat_falsificado ola.txt
$ Ola mundo cruel! Ola universo ingrato!

    7.Crie um código em C que conta a ocorrência de uma palavra-chave em um arquivo-texto, e escreve o resultado no terminal. Reaproveite as funções já criadas nas questões anteriores. Por exemplo, considerando que o código criado recebeu o nome de 'busca_e_conta':

$ echo Ola mundo cruel! Ola universo ingrato! > ola.txt
$ ./busca_e_conta Ola ola.txt
$ 'Ola' ocorre 2 vezes no arquivo 'ola.txt'.


