#include <stdio.h>
#include <stdlib.h>

int main() {
	unsigned int x[200];
	int y; 
	int z; 
	int k;
	int w;
	int j; 
	int i; 
	
	// ##########################################

	// O vetor x é utilizado para representar 200 "caixas" onde será possivel armazenar até 32 números em cada caixa (Do 0 ao 31).
	// Os 32 bits de cada inteiro de cada posição são utilizados para representar os 32 números de cada caixa.
	
	for(i = 0; i < 200; i++) { // inicializa o vetor com zeros onde serão armazenados os valores digitados
		x[i] = 0;
	}
	
	printf("Digite um numero entre 0 e 5000: ");
	scanf("%d", &k);
	
	while(k != -1) {
			z = 1;
		
			// "Z" é o valor que ao fazer o OU lógico na caixa, ativa o bit que representa o número digitado.

			for(i = 1; i <= k%32; i++) { // mapeia em potência de 2 a posição do bit que será ativo dentro da caixa.
				z = z * 2;
			}
			
			// K/32 calcula qual a caixa o numero será adicionado. 

			x[k/32] = x[k/32] | z;	// adiciona a lista de números.
				
		printf("Digite um numero entre 0 e 5000: ");
		scanf("%d", &k);
	}
	
	printf("\n\n");
	
	
	for(j = 5000; j >= 0; j--) { // percorre todos os números, de 5000 a 0 , procurando quem está ativo para imprimir na tela.
		z = 1;
			
		for(i = 1; i <= j%32; i++) { // mapeia em potência de 2 a posição do bit que será verificado se está ativo dentro da caixa.
			z = z * 2;	
		}
		
		if( (x[j/32] & z) != 0 ) { // Verifica com o & lógico se o bit está ativo na caixa para imprimir.
			printf("%i ", j);
		}
	}
	
	// ##########################################
	
	return 0;
}
