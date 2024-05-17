# rock-paper-scissors-game
package practice;

import org.w3c.dom.ls.LSOutput;

import java.util.Random;
import java.util.Scanner;

public class RockPaperScissor {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);


        while (true) {
            String[] rps = {"r", "p", "s"};
            String computerMove = rps[new Random().nextInt(rps.length)];
            String playerMove;
            while (true) {
                System.out.println("Please enter  your move(r,p, or s)");
                playerMove = sc.nextLine();
                if (playerMove.equals("r") || playerMove.equals("") || playerMove.equals("s")) {
                    break;
                }
                System.out.println(playerMove + "Pleased enter teh valid move");
            }
            // tie
            System.out.println("computer played:" + computerMove);
            if (playerMove.equals(computerMove)) {
                System.out.println("the game wash tie");
            }
            // 1st condition
            else if (playerMove.equals("r")) {
                if (computerMove.equals("p")) {
                    System.out.println("you loose");
                } else if (computerMove.equals("s")) {
                    System.out.println("you win");
                }
            }
            // 2nd condition
            else if (playerMove.equals("p")) {
                if (computerMove.equals("r")) {
                    System.out.println("you win");

                } else if (computerMove.equals("s")) {
                    System.out.println("you loose");
                }
            }
            // 3rd condition
            else if (playerMove.equals("s")) {
                if (computerMove.equals("p")) {
                    System.out.println("you win");
                } else if (computerMove.equals("r")) {
                    System.out.println("you loose");
                }
            }
            System.out.println("wanna play again? (y/n)");
            String playAgain= sc.next();
             if(playAgain.equals("y")){
                 break;
             }
        }
    }
}
