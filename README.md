#include <stdio.h>

void main() {
    int i, j, k;
    int m1, n1, m2, n2;
    int a[10][10], b[10][10], c[10][10] = {0};

    printf("Enter the rows and columns of matrix A:\n");
    scanf("%d %d", &m1, &n1);
    printf("Enter the rows and columns of matrix B:\n");
    scanf("%d %d", &m2, &n2);

    // Correct condition for matrix multiplication
    if (n1 != m2) {
        printf("Matrix multiplication is not possible.\n");
        return;
    }

    printf("Enter the elements of matrix A:\n");
    for (i = 0; i < m1; i++) {
        for (j = 0; j < n1; j++) {
            scanf("%d", &a[i][j]);
        }
    }

    printf("Enter the elements of matrix B:\n");
    for (i = 0; i < m2; i++) {
        for (j = 0; j < n2; j++) {
            scanf("%d", &b[i][j]);
        }
    }

    // Matrix multiplication
    for (i = 0; i < m1; i++) {
        for (j = 0; j < n2; j++) {
            c[i][j] = 0; // Optional, already initialized
            for (k = 0; k < n1; k++) {
                c[i][j] += a[i][k] * b[k][j];
            }
        }
    }

    printf("The resultant matrix is:\n");
    for (i = 0; i < m1; i++) {
        for (j = 0; j < n2; j++) {
            printf("%d ", c[i][j]);
        }
        printf("\n");
    }
}