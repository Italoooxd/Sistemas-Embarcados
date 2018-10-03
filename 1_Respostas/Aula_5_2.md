

Para todas as questões, utilize as funções da norma POSIX (open(), close(), write(), read() e lseek()). Compile os códigos com o gcc e execute-os via terminal.

    1.Crie um código em C para escrever "Ola mundo!" em um arquivo chamado 'ola_mundo.txt'.
 ```C

#include <stdio.h>
#include <stdlib.h>
#include <fcntl.h>
#include <unistd.h>



int main(int argc, const char * argv[]) {
  int fp;
  int ola;
  char string[100] = "Ola mundo !!\n";
  
  fp = open("ola_mundo.txt",O_WRONLY | O_CREAT);
  ola = write(fp, string, sizeof(string));
  close(fp);
  return 0;
}

 ```

    2.
```C
#include <stdio.h>
#include <stdlib.h>
#include <fcntl.h>
#include <unistd.h>
#include<string.h>



int main(int argc, const char * argv[]) {
  int fp;
  char nomef [100]= "Nome: ";
  char idadef [100]= "Idade: ";
  int i;
  int a;
  char nome[100];
  char nome1[100];
  char idade[100];
  


  
  printf("Digite seu nome: ");
  scanf("%s",nome);
  strcat(nomef, nome);
  strcat(nome,".txt");
  printf("Digite sua idade: ");
  scanf("%s",idade);
  strcat(idadef, idade);  
  strcat(idadef,"\n");
  fp = open(nome,O_WRONLY | O_CREAT, S_IRWXU);
  write(fp,nomef,sizeof(nomef));
  write(fp,"\n",1);
  write(fp,idadef,sizeof(idadef));
  //write(fp,"\n",1);
  
  close(fp);
   return 0;
}

```
    3.
```C
#include <stdio.h>
#include <stdlib.h>
#include <fcntl.h>
#include <unistd.h>
#include<string.h>



int main(int argc, const char * argv[]) {
  int fp;
  char nomef [100]= "Nome: ";
  char idadef [100]= "Idade: ";
  int i;
  int a;
  char nome[100];
  char nome1[100];
  char idade[100];
    


  
  //printf("Digite seu nome: ");
  strcpy(nome,argv[1]);
  strcat(nomef, nome);
  strcat(nome,".txt");
  //printf("Digite sua idade: ");
  strcpy(idade,argv[2]);
  strcat(idadef, idade);  
  strcat(idadef,"\n");
  fp = open(nome,O_WRONLY | O_CREAT, S_IRWXU);
  write(fp,nomef,sizeof(nomef));
  write(fp,"\n",1);
  write(fp,idadef,sizeof(idadef));
  //write(fp,"\n",1);
  
  close(fp);
   return 0;
}
```
    4.Crie uma função que retorna o tamanho de um arquivo, usando o seguinte protótipo: int tam_arq_texto(char *nome_arquivo); Salve esta função em um arquivo separado chamado 'bib_arqs.c'. Salve o protótipo em um arquivo chamado 'bib_arqs.h'. Compile 'bib_arqs.c' para gerar o objeto 'bib_arqs.o'.

    5.Crie uma função que lê o conteúdo de um arquivo-texto e o guarda em uma string, usando o seguinte protótipo: char* le_arq_texto(char *nome_arquivo); Repare que o conteúdo do arquivo é armazenado em um vetor interno à função, e o endereço do vetor é retornado ao final. (Se você alocar este vetor dinamicamente, lembre-se de liberar a memória dele quando acabar o seu uso.) Salve esta função no mesmo arquivo da questão 4, chamado 'bib_arqs.c'. Salve o protótipo no arquivo 'bib_arqs.h'. Compile 'bib_arqs.c' novamente para gerar o objeto 'bib_arqs.o'.

    6.Crie um código em C que copia a funcionalidade básica do comando cat: escrever o conteúdo de um arquivo-texto no terminal. Reaproveite as funções já criadas nas questões anteriores. Por exemplo, considerando que o código criado recebeu o nome de 'cat_falsificado':

$ echo Ola mundo cruel! Ola universo ingrato! > ola.txt
$ ./cat_falsificado ola.txt
$ Ola mundo cruel! Ola universo ingrato!

    7.Crie um código em C que conta a ocorrência de uma palavra-chave em um arquivo-texto, e escreve o resultado no terminal. Reaproveite as funções já criadas nas questões anteriores. Por exemplo, considerando que o código criado recebeu o nome de 'busca_e_conta':

$ echo Ola mundo cruel! Ola universo ingrato! > ola.txt
$ ./busca_e_conta Ola ola.txt
$ 'Ola' ocorre 2 vezes no arquivo 'ola.txt'.


