# Replace-all-0-s-with-1-in-a-given-integer-using-Java

Replace all 0’s with 1 using Java 
In this article we will create a  program to replace all 0’s with 1 using java. For this purpose we will ask the user to enter a positive number and check each digit one by one that it is equal to 0 or not. If the digit is equal to 0 then replace the digit by 1, and else no change.

Replace 0 with 1
Question can come like Way 1
Write a code to change all zero's as one's (0s as 1s) in a given number? ex: 120014 needs to be printed as 121114
Question can come like Way 2
implement a c program to replace all 0's with 1 in a given integer as an input, all the 0's in the number has to be replaced with 1.
Implementation
We will convert the integer into string.
Then we will convert it into list and then we will traverse through the list.
Wherever we find a ‘0’ we will replace with ‘1’.
Replace all 0's with 1 using java
Algorithm
Take Input in num and initialize a variable num with with value 0
If num is equals to zero then update the value of num2 to 1
Iterate using a while loop until num is greater then 0
For each iteration initialize a variable rem and store unit digit of num
If rem equals to 0 then set rem to 1
Set num to num divide by 10 & num2 equals to num2*10+rem
Reverse and print num2
Java code
Run
//Java program to replace all 0's with 1 in a given integer  : 
import java.util.Scanner;
public class Main
{
	public static void main(String[] args)
	{
		//scanner class declaration
		Scanner sc = new Scanner(System.in);
		//input from the user		
		System.out.print("Enter the number : ");		
		int number = sc.nextInt();
		//convert the number to string and then calculate its length
		String str = Integer.toString(number);
		int len = str.length();
		String str1 = "";
		//use the logic to replace all 0's with 1 in a given integer
		for(int i = 0 ; i < len ; i++)
		{
			if(str.charAt(i) == '0')
				str1 = str1 + '1';
			else
				str1 = str1 + str.charAt(i);	
		}
		System.out.println("Converted number is: "+str1);
		//closing scanner class(not compulsory, but good practice)
		sc.close();									
	}
}
Output
Enter the number : 706120678
Converted number : 716121678
