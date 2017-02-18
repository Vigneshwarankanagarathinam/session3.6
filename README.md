Session 3
Assignment 6 

1)	Can you overload a method with the same return type? Explain your answer with proper logic.
  
  Yes we can overload method with same return type but the argument list should be different. If it is the case that arguments are same as that of the other then at least the sequence of the arguments should be changed.
  Method Overloading means to have two or more methods with same name in the same class with different arguments. The benefit of method overloading is that it allows you to implement methods that support the same semantic operation but differ by argument number or type.

Important Points:

Overloaded methods MUST change the argument list
Overloaded methods CAN be done by changing the return type
Overloaded methods CAN change the access modifier
A method can be overloaded in the same class or in a subclass

import java.util.*;

public class acad
{
public static int acadgild(int num1 , int num2)
    {
		int sum=num1+num2;
		return sum;
	}
public static int acadgild(String string)
{
	int i=0,n,sum=0;
	while(i<string.length()) 
	{
		char c=string.charAt(i);	//getting each word from the string
		n = c;	//assigning ASCII value of each character to integer variable 
		sum=sum+n; //adding ASCII values
		i=i+1;
	}
	return sum;
}
public static void main(String args[])
{
	Scanner ss= new Scanner(System.in);
	System.out.println("Enter two numbers to be added:");
	int num1 = Integer.parseInt(ss.nextLine());	
	int num2 = Integer.parseInt(ss.nextLine());
	System.out.println("Enter a String:");
	String string= ss.nextLine();
	System.out.println("--Using Overloaded methods--");
	System.out.println("Output using Overloaded methods:");
	System.out.println("Sum of two numbers is "+acadgild(num1,num2));   //sum with integer type as input
	System.out.println("Sum of ASCII values of string is "+acadgild(string));   // sum with char type as input
	}
}  
Here we can see that the method sum has the same return type but argument list is different one gives actual sum and the other gives the sum of the ASCII values of the character in the string.
  
2)	Write a program in Java using Arrays, which sorts the element in a descending order.

import java.util.*;

public class acad
{
	public static void main(String args[])
	{
		Scanner ss= new Scanner(System.in);
		Integer[] descend= new Integer[5];	//declaring an integer array of size 5
		System.out.println("Enter the array of 5 integers to be sorted");
		for (int i = 0; i < 5; i++)
		{
			descend[i]=ss.nextInt();	//getting value for array
		}
		Arrays.sort(descend, Collections.reverseOrder());	  //sorting the array in descending order
		System.out.println("Descending order of the given numbers is:");
		int n=descend.length;
		for (int i = 0; i < n; i++)
		{
			System.out.println(descend[i]);	//printing the array
		}
	}
}
