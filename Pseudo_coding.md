###PSEUDOCODE

-------------------------------------------------------------------------------------------------
Pseudo Code Examples:

This program calculates the Lowest Common multiple
for excessively long input values

function lcmNaive(Argument one, Argument two){

	Calculate the lowest common variable of Argument
	1 and Argument 2 by dividing their product by their
	Greatest common divisor product

	return lowest common multiple
end
}
function greatestCommonDivisor(Argument one, Argument two){
	if Argument two is equal to zero
		then return Argument one

	return the greatest common divisor

end
}

{
In the main function
	
print prompt "Input two numbers"
		
Take the first number from the user
Take the second number from the user

Send the first number and second number
to the lcmNaive function and print
the result to the user
}


Actual code:

// This program calculates the Lowest Common multiple
// for excessively long input values

import java.util.*;

public class LowestCommonMultiple {

	private static long
	lcmNaive(long numberOne, long numberTwo)
	{

		long lowestCommonMultiple;

		lowestCommonMultiple
			= (numberOne * numberTwo)
			/ greatestCommonDivisor(numberOne,
									numberTwo);

		return lowestCommonMultiple;
	}

	private static long
	greatestCommonDivisor(long numberOne, long numberTwo)
	{

		if (numberTwo == 0)
			return numberOne;

		return greatestCommonDivisor(numberTwo,
									numberOne % numberTwo);
	}
	public static void main(String args[])
	{

		Scanner scanner = new Scanner(System.in);
		System.out.println("Enter the inputs");
		long numberOne = scanner.nextInt();
		long numberTwo = scanner.nextInt();

		System.out.println(lcmNaive(numberOne, numberTwo));
	}
}
------------------------------------------------------------------------------------------------
Algorithm of linear search :

1. Start from the leftmost element of arr[] and 
one by one compare x with each element of arr[]. 
2. If x matches with an element, return the index. 
3. If x doesn’t match with any of elements, return -1. 

Here, we can see how the steps of a linear search program are explained in a simple, English language.

Pseudocode for Linear Search : 
 
FUNCTION linearSearch(list, searchTerm):
     FOR index FROM 0 -> length(list):
       IF list[index] == searchTerm THEN
           RETURN index
       ENDIF
       ENDLOOP
           RETURN -1
END FUNCTION

In here, we haven’t used any specific programming language but wrote the steps of a linear search in 
a simpler form which can be further modified into a proper program. 

Program:
A program is a set of instructions for the computer to follow. The machine can’t read a program directly,
because it only understands machine code. But you can write stuff in a computer language, and then a compiler 
or interpreter can make it understandable to the computer.
Program for Linear Search : 


// C++ code for linearly search x in arr[].  If x
// is present  then return its  location,  otherwise
// return -1
int search(int arr[], int n, int x)
{
    int i;
    for (i = 0; i < n; i++)
        if (arr[i] == x)
         return i;
    return -1;
}

Algorithm vs Pseudocode vs Program:

An algorithm is defined as a well-defined sequence of steps that provides a solution for a given problem, 
whereas a pseudocode is one of the methods that can be used to represent an algorithm. 
 
While algorithms are generally written in a natural language or plain English language, pseudocode is written 
in a format that is similar to the structure of a high-level programming language. Program on the other hand 
allows us to write a code in a particular programming language. 
 
So, as depicted above you can clearly see how the algorithm is used to generate the pseudocode which is further 
expanded by following a particular syntax of a programming language to create the code of the program. 

-----------------------------------------------------------------------------------------------------------------------
S.NO	Algorithm							Flowchart
1.	Algorithm is step by step procedure to solve the problem.	Flowchart is a diagram created by different shapes to show the flow of data.
2.	Algorithm is complex to understand.				Flowchart is easy to understand.
3.	In algorithm plain text are used.				In flowchart, symbols/shapes are used.
4.	Algorithm is easy to debug.					Flowchart it is hard to debug.
5.	Algorithm is difficult to construct.				Flowchart is simple to construct.
6.	Algorithm does not follow any rules.				Flowchart follows rules to be constructed.
7.	Algorithm is the pseudo code for the program.			Flowchart is just graphical representation of that logic.

