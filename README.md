# School-Programming3
The third programming project in my class

package Chapter5PPMatthewRoberts;

import java.util.*;

public class Chapter5PPMatthewRoberts {

	public static void main(String[] args) {
		String name="name", quit="n", request="yes or no";
		
		
		
		int attending;
		final int CAPACITY = 30;
		
		Scanner scan = new Scanner(System.in);
		
		while (true) {
			if (request.equalsIgnoreCase(quit))
				break;	
			System.out.println("Welcome to the Meeting System. May I know your name? ");//greet user and ask for their name.
			name = scan.nextLine();
			System.out.println("Hello " + name + ", how many people are attending the meeting? "); //ask how many are attending the meeting.
			attending = scan.nextInt();
			if (attending < CAPACITY) { //If attending people is less than the capacity choose this message.	
				System.out.println("Wonderful, the room is pretty big. You can still invite " + (CAPACITY - attending) + " people to the meeting.");}
			else if (attending > CAPACITY) {//If attending people is more than the capacity choose this message.
				System.out.println("Sorry, but the room is not big enough. You have to exclude " + (attending - CAPACITY) + " people from the meeting.");}
			else if (attending == CAPACITY) {//If attending people is equal to the capacity choose this message.
				System.out.println("That is perfect. The room has the exact number of seats you are asking for!");}
			scan.nextLine();
			scan.nextLine();
			
			System.out.println("Would you like to make another request?(y/n) ");/*if y is chosen keep in the loop. if n is chosen break the loop.*/

	}
}
}
