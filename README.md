33.1 LAB: Formatted output: No parking sign

Write a program that prints a formatted "No parking" sign as shown below. 
Note the first line has two leading spaces. 
For ALL labs, end with newline (unless otherwise stated).

  NO PARKING
2:00 - 6:00 a.m.

Solution: This one is pretty obvious, just match formatting.

===

33.2 LAB: Input: Mad Lib
Mad Libs are activities that have a person provide various words, which are then used to complete a short story in unexpected \(and hopefully funny) ways.
Complete a program that reads four values from input and stores the values in variables first_name, generic_location, whole_number, and plural_noun.
The program then uses the input values to output a short story. The first input statement is provided in the code as an example.

 Notes: To test your program in the Develop mode, pre-enter four values (in separate lines) in the input box and click the Run program button.
 The auto-grader in the Submit mode will test your program with different sets input of values.

 Ex: If the input values are:

Eric
Chipotle
12
cars

then the program uses the input values and outputs a story:

Eric went to Chipotle to buy 12 different types of cars

Ex: If the input values are:

Brenda
Philadelphia
6
bells

then the program uses the input values and outputs a story:

Brenda went to Philadelphia to buy 6 different types of bells

===

33.3 LAB: Convert to dollars
Given four values representing counts of quarters, dimes, nickels and pennies, output the total amount as dollars and cents.

Output each floating-point value with two digits after the decimal point, which can be achieved as follows:
print(f'Amount: ${dollars:.2f}')

Ex: If the input is:

4 
3
2
1
where 4 is the number of quarters, 3 is the number of dimes, 2 is the number of nickels, and 1 is the number of pennies, the output is:

Amount: $1.41
For simplicity, assume input is non-negative.

===

33.4 LAB: Driving costs

 Driving is expensive. 
 Write a program with a car's gas mileage (miles/gallon) 
 and the cost of gas (dollars/gallon) as floating-point 
 input, and output the gas cost for 20 miles, 75 miles, and 500 miles.

 Output each floating-point value with two digits after the 
 decimal point, which can be achieved as follows:
 print(f'{your_value1:.2f} {your_value2:.2f} {your_value3:.2f}')

 Ex: If the input is:

 20.0
 3.1599

 where the gas mileage is 20.0 miles/gallon and the cost of gas is $3.1599/gallon, the output is:

 3.16 11.85 79.00

===

 33.5 LAB: Input and formatted output: Right-facing arrow
 Given input characters for an arrowhead and arrow body, print a right-facing arrow.

Ex: If the input is:

 *
 
 Then the output is:

       
 ******
 ******
 ******
       

===

 33.6 LAB: Phone number breakdown

 Given an integer representing a 10-digit phone number, output the area code, prefix, and line number using the format (800) 555-1212.

 Ex: If the input is:

 8005551212
 the output is:

 (800) 555-1212
 Hint: Use % to get the desired rightmost digits. Ex: The rightmost 2 digits of 572 is gotten by 572 % 100, which is 72.

 Hint: Use // to shift right by the desired amount. Ex: Shifting 572 right by 2 digits is done by 572 // 100, which yields 5. (Recall integer division discards the fraction).

 For simplicity, assume any part starts with a non-zero digit. So 0119998888 is not allowed.

phone_number = int(input())

Solution One:  uses modulo and // as per the hints.
 commented out as it is the more convoluted solution

 area_code = phone_number // 10000000

 three = (phone_number // 10000) % 1000

 four = phone_number % 10000

 print(f'({area_code}) {three}-{four}')

 Solution Two: String Slicing
 This is the faster option. The int is converted to a string, 
 which is then sliced into the requisite components.

===

 33.7 LAB: Smallest number
 Instructor note:
 The skills required for this lab are covered in Chapter 5. Branching. To successfully complete this lab, review the content of Chapter 5, as well as the preceding chapters, and complete the Challenge Activities associated.

 Write a program whose inputs are three integers, and whose output is the smallest of the three values.

 Ex: If the input is:

 7
 15
 3
 the output is:

 3

 Solution: Take all inputs as members of a list, this allows you to utilized the built in min function 
 without needing to write your own min function.

===

 33.8 LAB: Exact change
 Instructor note:
 The skills required for this lab are covered in Chapter 5. Branching. 
 To successfully complete this lab, review the content of Chapter 5, 
 as well as the preceding chapters, and complete the Challenge Activities associated.

 Write a program with total change amount as an integer input, 
 and output the change using the fewest coins, one coin type per line. 
 The coin types are Dollars, Quarters, Dimes, Nickels, and Pennies. 
 Use singular and plural coin names as appropriate, like 1 Penny vs. 2 Pennies.

 Ex: If the input is:

 0 
 (or less than 0), the output is:

 No change 
 Ex: If the input is:

 45
 the output is:

 1 Quarter
 2 Dimes

===

 33.9 LAB: Output range with increment of 5

 Write a program whose input is two integers. Output the first integer and subsequent increments of 5 as long as the value is less than or equal to the second integer. End with a newline.

 Ex: If the input is:

 -15
 10

 the output is:

 -15 -10 -5 0 5 10 
 Ex: If the second integer is less than the first as in:

 20
 5
 the output is:

 Second integer can't be less than the first.
For coding simplicity, output a space after every integer, including the last.

 Solution:
 Essentially this question is to make sure you can
 iterate through a loop giving a range and an interval

 A for loop is used to do this

===

 33.10 LAB: Print string in reverse
 Instructor note:
 The skills required for this lab are covered in Chapter 6. Loops. To successfully complete this lab, review the content of Chapter 6, as well as the preceding chapters, and complete the Challenge Activities associated.

 Write a program that takes in a line of text as input, and outputs that line of text in reverse. The program repeats, ending when the user enters "Done", "done", or "d" for the line of text.

 Ex: If the input is:

 Hello there
 Hey
 done
 then the output is:

 ereht olleH
 yeH

 Solution: String Slicing inside a while loop

===

33.11 LAB: Fibonacci sequence

The Fibonacci sequence begins with 0 and then 1 follows. 
All subsequent values are the sum of the previous two, ex: 0, 1, 1, 2, 3, 5, 8, 13. 
Complete the fibonacci() function, which has an index n as parameter and returns the nth value in the sequence. 
Any negative index values should return -1.

Ex: If the input is: 7
the output is: 'fibonacci(7) is 13'

===

 33.12 LAB: Calculate average

 Complete the calc_average() function that has an integer list parameter and returns the average value of the elements in the list as a float.

 Ex: If the input list is:

 1 2 3 4 5
 then the returned average will be:

 3.0

===

    33.13 LAB: Warm up: Text analyzer & modifier
    Instructor note:
    The skills required for this lab are covered in Chapter 10. Strings. To successfully complete this lab, review the content of Chapter 10, as well as the preceding chapters, and complete the Challenge Activities associated.

    (1) Prompt the user to enter a string of their choosing. Output the string. (1 pt)

    Ex:

    Enter a sentence or phrase:
    The only thing we have to fear is fear itself.

    You entered: The only thing we have to fear is fear itself.
    (2) Complete the get_num_of_characters() function, which returns the number of characters in the user's string. We encourage you to use a for loop in this function. (2 pts)

    (3) Extend the program by calling the get_num_of_characters() function and then output the returned result. (1 pt)

    (4) Extend the program further by implementing the output_without_whitespace() function. output_without_whitespace() outputs the string's characters except for whitespace (spaces, tabs). Note: A tab is '\t'. Call the output_without_whitespace() function in main(). (2 pts)

    Ex:

    Enter a sentence or phrase: 
    The only thing we have to fear is fear itself.

    You entered: The only thing we have to fear is fear itself.

    Number of characters: 46
    String with no whitespace: Theonlythingwehavetofearisfearitself.

===

    33.14 LAB: Palindrome
 
    A palindrome is a word or a phrase that is the same when read both forward and backward. Examples are: "bob," "sees," or "never odd or even" (ignoring spaces). Write a program whose input is a word or phrase, and that outputs whether the input is a palindrome.
    
    Ex: If the input is:
    
    bob
    the output is:
    
    bob is a palindrome
    Ex: If the input is:
    
    bobby
    the output is:
    
    bobby is not a palindrome
    Hint: Start by removing spaces. Then check if a string is equivalent to it's reverse.

===

    33.19 LAB: Thesaurus
    Instructor note:
    The skills required for this lab are covered in Chapter 14. Files. To successfully complete this lab, review the content of Chapter 14, as well as the preceding chapters, and complete the Challenge Activities associated.
    
    Given a set of text files containing synonyms for different words, complete the main program to output the synonyms for a specific word. Each text file contains synonyms for the word specified in the file’s name, and each row within the file lists the word’s synonyms that begin with the same letter, separated by a space. The program reads a word and a letter from the user and opens the text file associated with the input word. The program then stores the contents of the text file into a dictionary predefined in the program. Finally the program searches the dictionary and outputs all the synonyms that begin with the input letter, one synonym per line, or a message if no synonyms that begin with the input letter are found.
    
    Hints: Use the first letter of a synonym as the key when storing the synonym into the dictionary. Assume all letters are in lowercase.
    
    Ex: If the input of the program is:
    
    educate
    c
    the program opens the file educate.txt, which contains:
    
    brainwash brief
    civilize coach cultivate
    develop discipline drill
    edify enlighten exercise explain
    foster
    improve indoctrinate inform instruct
    mature
    nurture
    rear
    school
    train tutor
    then the program outputs:
    
    civilize
    coach
    cultivate
    Ex: If the input of the program is:
    
    educate
    a
    then the program outputs:
    
    No synonyms for educate begin with a.

===

    33.20 LAB: Word frequencies (lists)
    Instructor note:
    The skills required for this lab are covered in Chapter 14. Files. To successfully complete this lab, review the content of Chapter 14, as well as the preceding chapters, and complete the Challenge Activities associated.
    
    Write a program that first reads in the name of an input file and then reads the file using the csv.reader() method. The file contains a list of words separated by commas. Your program should output the words and their frequencies (the number of times each word appears in the file) without any duplicates.
    
    Ex: If the input is:
    
    input1.csv
    and the contents of input1.csv are:
    
    hello,cat,man,hey,dog,boy,Hello,man,cat,woman,dog,Cat,hey,boy
    the output is:
    
    hello 1
    cat 2
    man 2
    hey 2
    dog 2
    boy 2
    Hello 1
    woman 1
    Cat 1
    Note: There is a newline at the end of the output, and input1.csv is available to download.

===

    34.13 PRACTICE: Manipulate CSV files
   Instructions:
   
   Create a Python solution to the following task. Ensure that the solution produces output in exactly the same format shown in the sample(s) below, including capitalization and whitespace.
   Task:
   
   Create a solution that accepts an input identifying the name of a CSV file, for example, "input1.csv". Each file contains two rows of comma-separated values. Import the built-in module csv and use its open() function and reader() method to create a dictionary of key:value pairs for each row of comma-separated values in the specified file. Output the file contents as two dictionaries.
   
   The solution output should be in the format
   
   {'key': 'value', 'key': 'value', 'key': 'value'}
   {'key': 'value', 'key': 'value', 'key': 'value'}
   
   Sample Input/Output:
   
   If the input is
   
   input1.csv
   
   then the expected output is
   
   {'a': '100', 'b': '200', 'c': '300'}
   {'bananas': '1.85', 'steak': '19.99', 'cookies': '4.52'}
   
   Alternatively, if the input is
   
   input2.csv
   
   then the expected output is
   
   {'d': '400', 'e': '500', 'f': '600'}
   {'celery': '2.81', 'milk': '4.34', 'bread': '5.63'}

===

    34.14 PRACTICE: Math module
   Instructions:
   
   Create a Python solution to the following task. Ensure that the solution produces output in exactly the same format shown in the sample(s) below, including capitalization and whitespace.
   Task:
   
   Create a solution that accepts an integer input. Import the built-in module math and use its factorial() method to calculate the factorial of the integer input. Output the value of the factorial, as well as a Boolean value identifying whether the factorial output is greater than 100.
   
   The solution output should be in the format
   
   factorial_value
   Boolean_value
   
   Sample Input/Output:
   
   If the input is
   
   10
   
   then the expected output is
   
   3628800
   True
   
   Alternatively, if the input is
   
   3
   
   then the expected output is
   
   6
   False

 This is pretty straightforward, just import the
   math module and use math.factorial to get your
   computed result, then assign a bool based on
   that value.

===

    34.15 PRACTICE: Import custom module
   Instructions:
   
   Create a Python solution to the following task. Ensure that the solution produces output in exactly the same format shown in the sample(s) below, including capitalization and whitespace.
   Task:
   
   Create a solution that accepts an integer input representing the age of a pig. Import the existing module pigAge and use its pre-built pigAge_converter() function to calculate the human equivalent age of a pig. A year in a pig's life is equivalent to five years in a human's life. Output the human-equivalent age of the pig.
   
   The solution output should be in the format
   
   input_pig_age is converted_pig_age in human years
   
   Sample Input/Output:
   
   If the input is
   
   8
   
   then the expected output is
   
   8 is 40 in human years

   Solution (NOTE: this code will NOT work outside of the zylabs environment)