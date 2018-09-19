

    1.Quais são as vantagens e desvantagens em utilizar:

(a) fork?
	
(b) threads?

	É possível ter varias threads em uma mesma aplição podem utilizar a mesma variável, risco de corrupção de dados                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      

    2.Quantas threads serão criadas após as linhas de código a seguir? Quantas coexistirão? Por quê?

(a)
```C
void* funcao_thread_1(void *arg);
void* funcao_thread_2(void *arg);

int main (int argc, char** argv)
{
	pthread_t t1, t2;
	pthread_create(&t1, NULL, funcao_thread_1, NULL);
	pthread_create(&t2, NULL, funcao_thread_2, NULL);
	pthread_join(t1, NULL);
	pthread_join(t2, NULL);
	return 0;
}
```
(b)
```C
void* funcao_thread_1(void *arg);
void* funcao_thread_2(void *arg);

int main (int argc, char** argv)
{
	pthread_t t1, t2;
	pthread_create(&t1, NULL, funcao_thread_1, NULL);
	pthread_join(t1, NULL);
	pthread_create(&t2, NULL, funcao_thread_2, NULL);
	pthread_join(t2, NULL);
	return 0;
}
```
    Apresente as características e utilidades das seguintes funções:

(a) pthread_setcancelstate()

(b) pthread_setcanceltype()

(DICA: elas são relacionadas à função pthread_cancel().)

