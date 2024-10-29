# Calculadora-Eleitoral
/******************************************************************************

Você foi contratado para desenvolver um programa que simule o processo de 
votação em uma eleição. O programa deve registrar os votos de cada eleitor. 
Os votos válidos serão 1 para o candidato A, 2 para o candidato B e 3 para voto 
nulo.

Por se tratar de uma simulação, o número máximo de cada votação é 10, ou seja, 
o programa irá solicitar 10 votos.

Após registrar todos os votos, o programa deve calcular e exibir o resultado da 
eleição, mostrando o total de votos de cada candidato

*******************************************************************************/

        #include <stdio.h>
        #include <unistd.h> //Biblioteca de tempo
    
    int main(){
        
        int a, b, c, votos = 0, numero = 0;
        
        a = 0; //Canditado A
        b = 0; //Candidato B
        c = 0; //Nulo
        
        
       
       while(votos < 10){
           
           printf("Bem-vindos à democracia! \n");
           printf("CANDIDATO A: Número 1. \n");
           printf("CANDIDATO B: Número 2. \n");
           printf("NULO C: Número 3. \n");
           
           //Ele coloca o número do Candidato.
            printf("\nVOTE!\n");
            printf("Candidato: ");
            scanf("%d", &numero);
            
            //Aqui ele vai acusar se o usuário digitar um número errado.
            while(numero < 0 || numero > 3){
                
                printf("Candidato inexistente, digite novamente! \n\n");
                printf("Candidato: ");
                scanf("%d", &numero);
            }
            
            
            if(numero > 0 && numero <= 3){
                if(numero == 1){
                a = a + 1;  // a++       
                }
                else if(numero == 2){
                b = b + 1;   //b++      
                }
                else if(numero == 3){
                c = c + 1;   //c++       
                }
            
            }
            
            //votos++; ou votos = votos+1
            votos = votos+1;
            printf("Total de votos %d \n", votos);
            printf("Voto realizado! \n\n");
            sleep(2); //Aqui ele espera 5 Segundos para reiniciar o programa.
            
        }
        
        printf("Eleição encerrada! \n\n");
        printf("Candidato A teve %d votos!\n", a);
        printf("Candidato B teve %d votos!\n", b);
        printf("Votos nulos teve %d votos!\n", c);
        
    
        return 0;
    }
