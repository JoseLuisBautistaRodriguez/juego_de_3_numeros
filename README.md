//# juego_de_3_numeros
//El equipo genera un número entre 0 y 10, el usuario tiene que adivinar que número es, tiene tres oportunidades.
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main (){

	srand(time(NULL));
	int numpc = rand() % 11 ;
		
	int numsu, live;
	
	live = 3 ;
	
	printf(" Estoy pensando en un numero del 0 al 10. Tienes 3 vidas.\n ¿Cual es?");  //vida 1 ------------------------------------------------------
	scanf("%i", &numsu);
	
	
	if (numpc == numsu){
		
		printf("¡Excelente! \n La pc tambien escogió %d \n", numpc);
		
	}
	if (numpc != numsu && numsu < 11 && numsu > 0 ){
		
		printf("\n Malas noticias usuario, no es, pero te doy otra oportunidad: ");
		live--;
	}
	
		else{
			printf("El numero que has ingresado no es valido, lee bien las instrucciones\n");
		}
	
	scanf("%i", &numsu); //vida 2	-------------------------------------------------------------------------------------------------------------------
	
		if (numpc == numsu){
		
		printf("¡Que wall, es correcto! \n La pc tambien escogio %d \n", numpc);
	
		}
		if (numpc != numsu && numsu < 11 && numsu > 0 ){
		
			printf("\n Malas noticias usuario, te dare una oportunidad y ya: ");
			live--;
		}
		
		else{
			printf("El numero que has ingresado no es valido, lee bien las instrucciones\n");
		}
		
	scanf("%i", & numsu); //vida 3	---------------------------------------------------------------------------------------------------------------------
	
		if (numpc == numsu){
		
			printf("¡Genial! ¡Es correcto! \n La pc tambien escogió %d \n", numpc);
			live++;
	
		}
		
		if (numpc != numsu && numsu < 11 && numsu > 0 ){
		
			live--;
		}
	
		if( live == 0 ){
		
			printf("\n Ya se termino usuario.\n La pc eligió %d. \n", numpc);
		}
	
		else{
			printf("El numero que has ingresado no es valido, lee bien las instrucciones\n");
		}
	
	system ("pause");
	return 0;
}
