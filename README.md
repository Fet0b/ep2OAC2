# EP2 — KNN sequencial e paralelo (OAC II)

Trabalho acadêmico (USP) que implementa o classificador **k-vizinhos mais próximos (KNN)** em C, em duas versões, para comparar o tempo de execução:

- `knn.c` — versão sequencial.
- `knnParalelo.c` — versão paralelizada com **OpenMP**.

Ambas normalizam os atributos (min-max), calculam a distância euclidiana e medem o tempo de previsão.

## Dados
Arquivos `dados_xtrain.txt`, `dados_ytrain.txt` e `dados_xtest_<N>.txt` (N de 10 a 10.000.000 amostras de teste).

## Compilar e executar
```bash
gcc -O2 -o knn knn.c -lm
gcc -O2 -fopenmp -o knn_paralelo knnParalelo.c -lm
./knn && ./knn_paralelo
```

> Projeto da graduação, publicado apenas para fins de estudo.
