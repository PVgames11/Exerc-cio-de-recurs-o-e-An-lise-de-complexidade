1 -
#include <stdio.h>

void imprimir_inverso(int n, int sequencia[]) {
    if (n == 0)
        return;
    printf("%d ", sequencia[n - 1]); 
    imprimir_inverso(n - 1, sequencia); 
}

int main() {
    int n;
    printf("Digite o valor de n: ");
    scanf("%d", &n);

    int sequencia[n];
    printf("Digite os %d números:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &sequencia[i]); 
    }

    printf("Sequência na ordem inversa: ");
    imprimir_inverso(n, sequencia); 

    return 0;
}
 Ánalise assintotica - A entrada de dados será n vezes e a recursão será também n vezes,ou seja será O(n)

2 -   Sequência Fibonacci de maneira recursiva
#include <stdio.h>

int fibonacci(int num) {
    if (num <= 1)
        return num;
    return fibonacci(num - 1) + fibonacci(num - 2);

}

int main() {
    int num;
    printf("Digite o número que você deseje descobrir a sequência de Fibonacci:\n");
    scanf("%d",&num);
    printf("Resultado da sequência de Fibonacci até %d: %d\n", num, fibonacci(num));
    return 0;
}

Ánalise assintotica - Será O(2 levado a n),pois quanto mais aumenta o valor da entrada irá também aumentar o valor de execução do código


3 - SequÊncia de Fibonacci de maneira ITERATIVO
#include <stdio.h>

int main() {
    int n;
    printf("Digite o valor de n: ");
    scanf("%d", &n);

    int a = 0, b = 1, resultado = 0;
    if (n == 0)
        resultado = a;
    else {
        for (int i = 2; i <= n; i++) {
            resultado = a + b;
            a = b;
            b = resultado;
        }
    }

    printf("Resultado da sequência de Fibonacci até %d: %d\n", n, resultado);
    return 0;
}

Ánalise assíntotica - Será O(n) pois ele  executa um loop simples n vezes para calcular cada valor de Fibonacci, e a quantidade realizado de cada loop é constante.
