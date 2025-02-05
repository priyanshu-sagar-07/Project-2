import java.util.Random;
import java.util.Scanner;

public class GuessingGame {

    public static void main(String[] args) {
        // Initialize the Scanner for user input
        Scanner scanner = new Scanner(System.in);

        // Generate a random number between 1 and 100
        Random random = new Random();
        int randomNumber = random.nextInt(100) + 1;

        // Initialize the number of attempts
        int attempts = 0;

        // Start the game loop
        System.out.println("Welcome to the Guessing Game!");
        System.out.println("I've chosen a number between 1 and 100.");
        System.out.println("Can you guess it?");

        while (true) {
            // Prompt the user for their guess
            System.out.print("Enter your guess: ");
            int guess = scanner.nextInt();

            // Increment the number of attempts
            attempts++;

            // Compare the guess to the random number
            if (guess < randomNumber) {
                System.out.println("Too low! Try again.");
            } else if (guess > randomNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You guessed it in " + attempts + " attempts.");
                break;
            }
        }
    }
}
