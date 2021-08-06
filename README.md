// desafio-moto

/*
Joana adora brincar com números ímpares. No outro dia, ela começou a escrever, em cada linha, um número ímpar de números ímpares. Parecia como se segue:
1
3  5  7
9 11 13 15 17
19 21 23 25 27 29 31
...

Em uma determinada linha Joana escreveu 55 números ímpares. Vôce pode descobrir a soma dos últimos três números escritos nessa linha? Você pode fazer isso em geral, para uma determinada quantidade de números ímpares?

Dado o número N, que representa uma determinada linha, a sua tarefa é a de determinar a soma dos três últimos números da linha.

Formato de entrada 
A entrada é um número N (1 < N <= 1.000.000.000).

Formato de saída
Escrever a soma dos três últimos números ímpares escritos por Joana na linha N, seguido por uma quebra de linha.

Exemplo de Entrada
3

Exemplo de saída
45

*/


```

import java.util.List;
import java.util.ArrayList;

public class Triangle {
    public static void main(String[] args) {
        int max_num_ints = 16;
        List<int[]> matrix = new ArrayList<>();

        int row_size = 1;
        int valor = 1;
        for (int i = 0; (valor -1) / 2 < max_num_ints; i++) {
            matrix.add(new int[row_size]);
            for (int j = 0; j < row_size; j++) {
                matrix.get(i)[j] = valor;
                valor += 2;
            }
            row_size += 2;
        }
        // printTriangle(matrix); for testing
        printSumLastThree(matrix);
    }

    public static void printTriangle(List<int[]> matrix) {
        for (int i = 0; i < matrix.size(); i++) {
            for (int j = 0; j < matrix.get(i).length; j++) {
                System.out.print(matrix.get(i)[j] + " ");
            }
            System.out.println("");
        }
    }

    public static void printSumLastThree(List<int[]> matrix) {
        int[] row = matrix.get(matrix.size()-1);
        int rowLength = row.length;
        System.out.println(row[rowLength - 1] + row[rowLength - 2] + row[rowLength - 3]);
    }
}
```
