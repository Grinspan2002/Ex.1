General instructions
The T.A responsible for this exercise is Eliyahu Houri.

You must fork the repository ex1 from the course’s git.
Change ex1.c according to instructions.
After completing all the requirements, submit it to the submit system under ex1 til 19\11\25 at 23:59:59.
Your submission should be a zip file containing:
.git folder (after fork and clone, as you did in ex0).
ex1.c
README.md (optional)
Late submissions will be fined accordingly:
One day - 10 points. (the maximum grade is 90)
Two days - 20 points.
Three days - 30 points.
You can’t submit this or any other exercise more than 3 days late.
Please post any questions about the exercise publicly in the course forum.
Requests for an extension (for justified reasons only) should be sent to the email: CSI.BIU2024@gmail.com with:
Full Name.
Your Submit system username.
ID.
The input and output design instructions must be read carefully, exactly according to the attached examples.
There are executable programs (windows and Linux) in the forum, you can run them on your computer and it may help you understand better.
The automation grading system checks that your output is the same as the expected output and therefore your output must be exactly the same as the examples.
As so, there is a Coding Style file in the forum - read it and work accordingly.
Testing your code on the server is highly recommended to ensure there are no warnings or errors.
An exercise that will have warning(s) or error(s) will get a fine that can reach 100 points.
You are reminded that thinking together is a blessing, working together is cheating.
An exercise that the system will catch as a “copy” will result in 0 - for everyone involved, and additional actions will take place.

In the development of your code, you can use any work environment.
The main thing is that you know how to take the code files from this environment, check them on the university servers, and submit them using the submission system.
Please note that you submit only the files containing your code, and not unnecessary files created by the work environment.
Also, DO NOT submit files/folders with names containing Hebrew characters.
Please note that it is not possible to copy a file with a path containing Hebrew characters to the university's servers.

This exercise compile command (Linux) is:
gcc -std=c99 -Wall -Wextra -Werror -DNDEBUG ex1.c -o ex1.out -lm


Mission instructions
In this exercise, you need to write a single program that does a few tasks, one after another.
Each task is quite short and most of them are similar.
Please notice, no matter your previous knowledge, in this task you may use only printf, scanf, getchar, and bitwise operations.
You can’t use any control flow or functions.


The file ex1.c is already created and you can see it here: https://github.com/CSI-BIU/ex1
Just fork the repository and work on the file on your computer.
There are comments to help you inside the files, but the full explanation will be in this document.

The following sections provide examples in 8-bit, but they are just as relevant to 32-bit.
Moreover, the examples are with different colors for your convenience, you obviously do not need [and not allowed] to change the color your program will output.

Please note:
Input integrity can be assumed.
There are assumptions per task in the relevant tasks.
This color is for input.
This color is for not textual output.


First task - Ascii
In this part, you need to get one character from the user.
Then, refer to it as an integer.
a. Print its value.
b. Print “0”, if its integer representation is even. print “1” if its integer representation is odd.
You can assume it won’t be a whitespace character.
Example:

explanation:
A’s numerical value is 65, and it is obviously an odd number.


Second task - 2’s complement to other representations
In this part, you will get a negative integer. [2’s complement].
Print its value in 1’s complement.
Print its value as unsigned.
You can use the char  “-” only for this task. [and you can not use “+”]
Example:

explanation:
-2 in 2’s complement is:
1111 1110
But in 1’s complement:
1111 1110 -> 0000 0001 = 1 -> -1
And the unsigned value of 31 bits of 1 and LSB 0 - is 4294967294

Third task - Shifting right and left
In this part, you will get 3 integers.
The first one - the value you will play with.
The second and the third - how much to shift right and left, respectively.
Print the value after shifting right and then shifting left.
You can assume the first integer is positive, and that integers 2 and 3 are less than 32.
Example:

explanation:
71 in binary is 0100 0101
Shifting it 5 to the right will result in: 0000 0010
And then 3 to the left will result in: 0001 0000
Which you already see in less than a second it is 16.


Fourth task - Even - odd
In this part, you will get 3 Integers.
If at least two of them are even - print 0.
If at least two of them are odd - print 1.

Example:

explanation:
I believe you got it alone.


Fifth task - Different Bases
In this part, you need to get two numbers, one in octal base, one in Hexadecimal base.
Print their LSB’s.
Print their MSB’s.

Example:

explanation:
We are handling 32 bits.
1234567 is 000 … 001 010 011 100 101 110 111
8000000 is 1000 0000 0000 0000 0000 0000 0000 0000


Complete code example:
Please notice the print before each task, the new lines between each task, and the “Bye!” at the end [There is no \n after it].
You can copy from here if you wanna make sure it’s exactly the same.
Don’t worry, when you submit the file - you will see if the output is exactly the same or not 🙂

Ascii:
Please enter a character
A
Its numerical value is: 65
0 for even, 1 for odd: 1

2’s complement to other representations:
Please enter a negative integer
-2
1's complement: -1
unsigned: 4294967294

Shifting right and left:
Please enter 3 integers
71 5 3
After shifting right and left: 16

Even - Odd:
Please enter 3 integers
5 -4 100
0 - most of them are even, 1 - most of them are odd: 0

Different Bases:
Please enter two numbers in octal and hexadecimal bases
1234567 80000000
LSBs: 1 0
MSBs: 0 1
Bye!
