# Abhik-preWorkAssignmentSolution
import java.util.Scanner;
public class Assessment 
{

	public static void main(String[] args) 
	{
		Scanner sc = new Scanner(System.in);
		System.out.println("1. Find palindrome of number");
		System.out.println("2. Print Pattern for a given number");
		System.out.println("3. Check whether the number is a  prime number");
		System.out.println("4. Print Fibonacci series");
		System.out.println("Please Enter your choice: ");
		int ch = sc.nextInt();
		switch(ch)
		{
		case 1:
			System.out.println("Enter the number");
			int number = sc.nextInt();
	        int temp=number;
	        int rev=0,rem;
	        while(temp!=0)
	        {
	        	rem=temp%10;
	        	rev=rev*10+rem;
	        			temp=temp/10;
	        }
	        if(number==rev)
	        {
	        	System.out.println(number+"is palindrome number");
	        }
	        else
	        {
	        	System.out.println(number+"is not palindrome number");
	        }
	        break;
		case 2:
			System.out.println("Enter the number of rows needed to print the pattern ");
			int rows = sc.nextInt();
			for (int i=1; i<=rows; i++) 
	        { 
	            for (int k=rows; k>=i; k--)
	            {
	                System.out.print("*");
	            }
	            for (int j=1; j<i; j++)
	            {
	                System.out.print(" ");
	            }
	            
	            System.out.println();
	        }
			break;
		case 3:
			System.out.println("Enter the no");
			int no = sc.nextInt();
	        int temp1=0;
	        for (int i=2; i<=no-1; i++) 
	        {
	        	if(no%i==0)
	        	{
	        		temp1=temp1+1;
	        	}
	        }
	        if(temp1==0)
	        {
	        	System.out.println(no+"is prime nunber");
	        }
	        else
	        {
	        	System.out.println(no+"is not prime number");
	        }
			break;
		case 4:
			int n , first = 0 , next = 1;
			System.out.println("Enter how many fibonnaci number to print");
	        n= sc.nextInt();
	        System.out.print("The first"+n+"fibonacci numbers are:");
	        System.out.print(first+" "+next);
	        int i = 1;
	        while(i<n-1)
	        {
	        	int sum = first +next;
	        	first = next;
	        	next = sum;
	        	System.out.print(" "+sum);
	        	i++;
	        }
	        	break;
	        default :
	        	System.out.println("Invalid choice. Enter a valid no ");
	        
		}
		while (ch != 0);

		System.out.println("Exited Successfully!!!");

		sc.close();

	}

}
