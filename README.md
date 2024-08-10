#include <stdio.h>
#include<stdlib.h>
#include<time.h>

int main() {

/*
project 1 = write a progam that generates a random numeberand ask the player 
to guess it. If the player's guess is higher than the actual numeber, the 
program displayes "lower number please". Similarly if the user guess it to low,
the program prints "higher number please".
When the user guessses the correct number,the program display the number 
of guesses the player used to arrive at the number 

hint : use loops 
use  a random number generater : which i use from chat gpt
*/
    // Initialize the random number generator with the current time
    srand(time(NULL));

    // Generate a random number between 1 and 100
    int randomNumber = (rand() % 100) + 1;
    int no_of_guesses = 0;
    int guessed;

    // // Print the generated random number
    // printf("Random number between 1 and 100: %d\n", randomNumber);
   do{
    printf("guess the number ");
     scanf("%d", &guessed);
     if(guessed>randomNumber){
        printf("lower number please!\n");
     }
     else if(guessed<randomNumber){
        printf("higher number please!\n");
     }
     else {
      printf("congrats!!\n");
     }
   no_of_guesses++;
   }while(guessed!= randomNumber);
    

printf("you guessed the number in %d guesses ", no_of_guesses);

    
    return 0;
}# first-guess-game
