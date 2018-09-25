

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
R: O POSIX (Interface Portátil para Sistemas Operacionais) é uma família de padrões especificados pelo IEEE para manter a compabtibilidade entre sistemas operacionais.
    
(a) Quais são as funções (e seus protótipos) para abrir e fechar arquivos?
```C
int open(const char *pathname, int flags, mode_t mode);
int close(int fildes);
```
(b) Quais são as funções (e seus protótipos) para escrever em arquivos?
```C
ssize_t write(int fd, const void *buf, size_t count);
```
(c) Quais são as funções (e seus protótipos) para ler arquivos?
```C
ssize_t read(int fd, void *buf, size_t count);
```
(d) Quais são as funções (e seus protótipos) para reposicionar um ponteiro para arquivo?
```C
off_t lseek(int fd, off_t offset, int whence);
```
(e) Quais bibliotecas devem ser incluídas no código para poder utilizar as funções acima?
```C
<sys/types.h>, <sys/stat.h>, <fcntl.h> e <unistd.h>
```
