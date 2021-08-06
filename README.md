# desafio-moto

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
