# Binary-to-decimal-conversion-using-Java

Binary to decimal conversion
 
In this article we will discuss binary to decimal conversion using java. For this purpose we need to ask a binary number from user and convert that binary number to its decimal equivalent form and then print the converted number on to the screen.
 
Binary to decimal conversion
Working :
 A Decimal number can be calculated by multiplying every digits of binary number with 2 to the power of the integers

 starts from 0 to n-1 where n refers as the total number of digits present in a binary number and finally add all of them.

Algorithm :
While num is greater then zero
Store the unit place value of num to a variable (rem)
Calculate rem with base and add it to answer
Completely divide Num by 10 and multiply base with 2
Binary to decimal conversion using java
Java Code :
Run
 

//Java program to convert Binary number to decimal number
import java.util.Scanner;
public class Main
{
	public static void main(String args[])
	{
		Scanner sc = new Scanner(System.in);    
		System.out.print("Enter a binary number : ");
		int binary = sc.nextInt();
		//Declaring variable to store decimal number  
		int decimal = 0;
		//Declaring variable to use in power		
		int n = 0;  
		//writing logic for the conversion
		while(binary > 0)
		{
			int temp = binary%10; 
			decimal += temp*Math.pow(2, n);  
			binary = binary/10;  
			n++;  
		}
		System.out.println("Decimal number : "+decimal); 
                //closing scanner class(not compulsory, but good practice)
		sc.close();
	}
}
Output :
Enter a binary number : 111001
Decimal number : 
