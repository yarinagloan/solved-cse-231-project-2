Download Link: https://assignmentchef.com/product/solved-cse-231-project-2
<br>
This assignment focuses on the design, implementation and testing of a Python program which uses control structures to solve the problem described below.

It is worth 20 points (2% of course grade) and must be completed no later than <strong>11:59 PM on Monday, January 20</strong>.




<h2>Assignment Overview</h2>

(learning objectives)

This assignment will give you more experience on the use of:

<ul>

 <li>integers (int)</li>

 <li>conditionals iteration</li>

 <li>input/output</li>

</ul>




<h2>Assignment Specifications</h2>

<strong> </strong>

The program will compute and display information for a company which rents vehicles to its customers.  For a specified customer, the program will compute and display the amount of money charged for that customer’s vehicle rental.




<ol>

 <li>The program should start by asking the user if he wants to continue. The answer is ‘Y’ for yes or ‘N’ for no. You can check the value with Boolean expressions such as</li>

</ol>

answer == ‘Y’

or    answer != ‘Y’.




The basic structure of the main loop is




Prompt to see if the user wants to continue While the value is ‘Y’:

All your other code goes here

Prompt to see if the user wants to continue




<ol start="2">

 <li>It will then continue to prompt the user to enter the following four items for a given customer (in the specified order):</li>

</ol>




<ol>

 <li>The customer’s classification code (a character)</li>

 <li>The number of days the vehicle was rented (an integer)</li>

 <li>The vehicle’s odometer reading at the start of the rental period (an integer)</li>

 <li>The vehicle’s odometer reading at the end of the rental period (an integer)</li>

</ol>




It will then process that customer information and display the results.  At the end, the program should ask the user if he wants to process another request and it will keep asking until the user enter 0.




<ol start="3">

 <li>The program will compute the amount of money that the customer will be billed, based on the customer’s classification code, number of days in the rental period, and number of miles driven. The program will <u>only</u> recognize both upper case letters for the classification codes.</li>

</ol>




Code ‘B’ (budget)




base charge:  $40.00 for each day




mileage charge:  $0.25 for each mile driven




Code ‘D’ (daily)




base charge:  $60.00 for each day




mileage charge:  no charge if the average number of miles driven per day is 100 miles or less; otherwise, $0.25 for each mile driven above the 100 mile per day limit.




Code ‘W’ (weekly)




base charge:  $190.00 for each week (or fraction of a week)




mileage charge:  no charge if the average number of miles driven per week is 900 miles or less; $100.00 per week if the average number of miles driven per week exceeds 900 miles but does not exceed 1500 miles; otherwise, $200.00 per week plus $0.25 for each mile driven above the 1500 mile per week limit.  (Note: if you rent for 8 days that is more than one week so the base rate is for 2 weeks – hint: use math.ceil().  Also, you are to take the total miles and subtract 1500*weeks to get the miles you will be charging for.)




The amount billed to the customer is the sum of the base charge and the mileage charge.




<ol start="4">

 <li>The program will compute the number of miles driven by the customer during the rental period. The odometer readings are taken from an odometer which has six digits and records tenths of a mile.</li>

</ol>




<ol start="5">

 <li>For each customer, the program will display a summary with the following information:</li>

</ol>




<ol>

 <li>The customer’s classification code</li>

 <li>The number of days the vehicle was rented</li>

 <li>The vehicle’s odometer reading at the start of the rental period</li>

 <li>The vehicle’s odometer reading at the end of the rental period</li>

 <li>The number of miles driven during the rental period</li>

 <li>The amount of money billed to the customer for the rental period</li>

</ol>




All output will be appropriately labeled and formatted.  The number of miles driven will be rounded to one fractional digit.  The amount of money billed will be displayed with a dollar sign and will be rounded to two fractional digits (for example, $125.99 or $43.87).  Note that we do not have the ability yet to fine tune the output so if cents end in zero that final zero will not be displayed—that is fine for this project.  We provide a file strings.txt with the strings we used to make it easier for you to match our output.




<ol start="6">

 <li>The program will detect, report and recover from invalid classification codes. When an invalid classification code is detected, the program will display an error message and re-prompt until a correct classification code is entered.</li>

</ol>




Hint: use a while loop that will loop until a correct classification code is entered.  Here is <em>pseudo code</em> of that loop:




Prompt for a value

While the value is not correct: Print an error message

Prompt for a value




<ol start="7">

 <li>The program will assume that all other user inputs are valid and correct. That is, the program will not check the number of days or odometer readings for validity.  However, as noted below you may encounter an ending odometer reading that is less than the beginning reading and you need to handle that correctly.</li>

</ol>







<h2>Assignment Deliverable</h2>

The deliverable for this assignment is the following file:

proj02.py – the source code for your Python program

Be sure to use the specified file name and to submit it for grading via the <strong>Mimir </strong>before the project deadline.

<strong> </strong>

<h2>Assignment Notes</h2>




<ol>

 <li>As stated above, the odometer’s dial has six digits and records tenths of a mile. For example, if the beginning reading was 100003 and the ending reading was 100135, then the customer drove 13.2 miles during the rental period.</li>

</ol>




<ol start="2">

 <li>Since the odometer’s dial is fixed with only six digits, the reading at the end of the rental period may be less than the reading at the beginning of the billing period. For example, if the beginning reading was 999997 and the ending reading was 000005, then the customer drove 0.8 miles during the rental period.  You need to handle that arithmetic correctly.</li>

</ol>




<ol start="3">

 <li>Be sure to prompt the user for the four inputs in the specified order and, your program cannot prompt the user for any supplementary inputs.</li>

</ol>




<ol start="4">

 <li>The structure of the main loop is as follows (in pseudo-code): Prompt for an input # for example,  answer = input(… while Boolean:   # Boolean expression uses input such as “answer”</li>

</ol>

# all your code goes here

Prompt for an input  (same statement used above)







<ol start="5">

 <li>It isn’t necessary for the user to type leading zeroes when entering odometer readings. However, it doesn’t hurt anything, either.</li>

</ol>




<ol start="6">

 <li>Coding Standards 1 – 6 will be enforced.</li>

</ol>




<ol start="7">

 <li>You are not allowed to use functions or advanced data structures such as lists, dictionaries, etc. That is, things we haven’t covered yet.</li>

</ol>




<ol start="8">

 <li><em>Beware</em> of this common programming error: you may be thinking of a Boolean expression this way:</li>

</ol>

x == ‘B’ or ‘D’ or ‘W’

However, that evaluates to True for any value of x because any <strong>non-empty</strong> string evaluates to

True so that Boolean expression is equivalent to

x = ‘B’ or True or True

whose value is True for any value of x.

The logically correct way to write that expression is




x == ‘B’ or x == ‘D’ or x == ‘W’




If you want the negation of that, you can do the following:




not(x == ‘B’ or x == ‘D’ or x == ‘W’)




Note that this next expression does <strong>not</strong> have the same value!




x != ‘B’ or x != ‘D’ or x != ‘W’)




Understanding why not is a useful exercise. (For the curious lookup DeMorgan’s Law.)







<strong> </strong>

<h2>Suggested Procedure</h2>

<strong> </strong>

<ul>

 <li><em>Solve the problem using pencil and paper first.</em> You cannot write a program until you have figured out how to solve the problem.  This first step is best done collaboratively with another student.  However, once the discussion turns to Python specifics and the subsequent writing of Python statements, you must work on your own.</li>

</ul>




<ul>

 <li>Write a simple version of the program. Run the program and track down any errors.</li>

</ul>




<ul>

 <li>Use the <strong>Mimir</strong> system to turn in the first version of your program.</li>

</ul>




<ul>

 <li>Cycle through the steps to incrementally develop your program:

  <ul>

   <li>Edit your program to add new capabilities.</li>

   <li>Run the program and fix any errors.</li>

  </ul></li>

</ul>




<ul>

 <li>Use the <strong>Mimir</strong> system to submit your final version.</li>

</ul>




<ul>

 <li>Be sure to log out when you leave the room, if you’re working in a public lab.</li>

</ul>










<strong> </strong>

<h2>Test 1</h2>




Welcome to car rentals.




At the prompts, please enter the following:

Customer’s classification code (a character: BDW)

Number of days the vehicle was rented (int)

Odometer reading at the start of the rental period (int)

Odometer reading at the end of the rental period (int)




Would you like to continue (Y/N)? N Thank you for your loyalty.




<h2>Test 2</h2>




Welcome to car rentals.




At the prompts, please enter the following:

Customer’s classification code (a character: BDW)

Number of days the vehicle was rented (int)

Odometer reading at the start of the rental period (int)

Odometer reading at the end of the rental period (int)




Would you like to continue (Y/N)? Y




Customer code (BDW): D




Number of days: 1

Odometer reading at the start: 100003

Odometer reading at the end:   100135  Customer summary:

classification code: D

rental period (days): 1

odometer reading at start: 100003  odometer reading at end:   100135     number of miles driven:  13.2

amount due: $ 60.0




Would you like to continue (Y/N)? Y




Customer code (BDW): D




Number of days: 4

Odometer reading at the start: 101010

Odometer reading at the end:   108200




Customer summary:

classification code: D

rental period (days): 4

odometer reading at start: 101010  odometer reading at end:   108200     number of miles driven:  719.0       amount due: $ 319.75




Would you like to continue (Y/N)? Y




Customer code (BDW): D




Number of days: 2

Odometer reading at the start: 002000

Odometer reading at the end:   004000




Customer summary:

classification code: D     rental period (days): 2

odometer reading at start: 2000  odometer reading at end:   4000       number of miles driven:  200.0

amount due: $ 120.0




Would you like to continue (Y/N)? Y




Customer code (BDW): B




Number of days: 3

Odometer reading at the start: 999997

Odometer reading at the end:   000005




Customer summary:

classification code: B     rental period (days): 3       odometer reading at start: 999997     odometer reading at end:   5  number of miles driven:  0.8

amount due: $ 120.2




Would you like to continue (Y/N)? N Thank you for your loyalty.

<strong> </strong>

<h2>Test 3</h2>




Welcome to car rentals.




At the prompts, please enter the following:

Customer’s classification code (a character: BDW)

Number of days the vehicle was rented (int)

Odometer reading at the start of the rental period (int)

Odometer reading at the end of the rental period (int)




Would you like to continue (Y/N)? Y




Customer code (BDW): D




Number of days: 3

Odometer reading at the start: 002000

Odometer reading at the end:   002100




Customer summary:

classification code: D     rental period (days): 3

odometer reading at start: 2000  odometer reading at end:   2100       number of miles driven:  10.0

amount due: $ 180.0




Would you like to continue (Y/N)? Y




Customer code (BDW): D




Number of days: 8

Odometer reading at the start: 000200

Odometer reading at the end:   010000




Customer summary:

classification code: D     rental period (days): 8

odometer reading at start: 200  odometer reading at end:   10000    number of miles driven:  980.0

amount due: $ 525.0




Would you like to continue (Y/N)? N

Thank you for your loyalty.

<em> </em>

<h2>Test 4</h2>







Welcome to car rentals.




At the prompts, please enter the following:

Customer’s classification code (a character: BDW)

Number of days the vehicle was rented (int)

Odometer reading at the start of the rental period (int)

Odometer reading at the end of the rental period (int)




Would you like to continue (Y/N)? Y




Customer code (BDW): W




Number of days: 8

Odometer reading at the start: 000100

Odometer reading at the end:   040100




Customer summary:

classification code: W     rental period (days): 8

odometer reading at start: 100  odometer reading at end:   40100    number of miles driven:  4000.0       amount due: $ 1030.0




Would you like to continue (Y/N)? Y




Customer code (BDW): W




Number of days: 6

Odometer reading at the start: 000100

Odometer reading at the end:   001000




Customer summary:

classification code: W     rental period (days): 6

odometer reading at start: 100  odometer reading at end:   1000       number of miles driven:  90.0

amount due: $ 190.0




Would you like to continue (Y/N)? N Thank you for your loyalty.

<strong> </strong>

<h2>Test 5</h2>

<strong> </strong>

Welcome to car rentals.




At the prompts, please enter the following:

Customer’s classification code (a character: BDW)

Number of days the vehicle was rented (int)

Odometer reading at the start of the rental period (int)

Odometer reading at the end of the rental period (int)




Would you like to continue (Y/N)? Y




Customer code (BDW): x




*** Invalid customer code. Try again. ***




Customer code (BDW): y




*** Invalid customer code. Try again. ***




Customer code (BDW): W




Number of days: 14

Odometer reading at the start: 000100

Odometer reading at the end:   001000




Customer summary:

classification code: W  rental period (days): 14     odometer reading at start: 100  odometer reading at end:   1000  number of miles driven:  90.0      amount due: $ 380.0




Would you like to continue (Y/N)? Y




Customer code (BDW): W




Number of days: 15

Odometer reading at the start: 000000

Odometer reading at the end:   028000




Customer summary:

classification code: W  rental period (days): 15     odometer reading at start: 0  odometer reading at end:   28000  number of miles driven:  2800.0    amount due: $ 870.0




Would you like to continue (Y/N)? Y




Customer code (BDW): W




Number of days: 10

Odometer reading at the start: 000100

Odometer reading at the end:   090000




Customer summary:

classification code: W  rental period (days): 10

odometer reading at start: 100  odometer reading at end:   90000  number of miles driven:  8990.0    amount due: $ 2277.5




Would you like to continue (Y/N)? N Thank you for your loyalty.

<strong> </strong>


