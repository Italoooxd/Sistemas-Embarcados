

    Considerando a biblioteca-padrão da linguagem C, responda:

(a) Quais são as funções (e seus protótipos) para abrir e fechar arquivos?
```C

FILE fp  =  *fopen ();
FILE fp = *fclose();

```

(b) Quais são as funções (e seus protótipos) para escrever em arquivos?

```C
int putc (int ch, FILE* fp)
```

(c) Quais são as funções (e seus protótipos) para ler arquivos?

```C
int getc (FILE *fp)

```

(d) Quais são as funções (e seus protótipos) para reposicionar um ponteiro para arquivo?

```C
int fseek (FILE stream, long int offset, int origin)

```

(e) Quais bibliotecas devem ser incluídas no código para poder utilizar as funções acima?
```C
#include <stdio.h>

```


    O que é a norma POSIX?

    Considerando a norma POSIX, responda:

(a) Quais são as funções (e seus protótipos) para abrir e fechar arquivos?

(b) Quais são as funções (e seus protótipos) para escrever em arquivos?

(c) Quais são as funções (e seus protótipos) para ler arquivos?

(d) Quais são as funções (e seus protótipos) para reposicionar um ponteiro para arquivo?

(e) Quais bibliotecas devem ser incluídas no código para poder utilizar as funções acima?

