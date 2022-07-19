## Create a simple Python game

In this blog post, I am going to be taking you on a step to step journey on how to build a simple python game. We will be building a guessing game in this section. There are many ways the guessing game can work. You could guess a number and play the game until the program you built guessed the correct number you had in mind, or the program can generate a random number that will be hidden and you have to guess the number. But for this section we would be doing the first, as I find it exciting that we have to think of a number and the program has to guess that number in 10 trials or less.

Let's get right into it......
First we define the lower range and the upper range of the numbers that a user is allowed to think of, this is because numbers are infinite, and it will be easier for the program to guess the number if it is within a particular range. Then we urge the user to think of a number within the range of the lower defined number to the higher defined number using a print function. The user has to Press enter to start, and we set the number of guesses to be one at first, this number will increase according to how many times the computer has to guess before it guessed the correct number you had in mind.


```
low = 1
high = 1000
print("Please think of a number between the range {0} and {1}".format(low, high))
input("Press Enter to start")
guesses = 0

``` 


Then we use a "while loop" for as long as the program doesn't guess what you had in mind, it repeats the block of code under the while statement, first it prints out the range at which it is guessing from first then it carries out a calculation to guess the number you had in mind, that calculation will make it easier for the program to be able to guess what you had in mind. The next line is an input line, where you either confirm if the program guessed what you thought of correctly or it has to guess higher or lower, you input "h" if it should guess higher, "l" if it should guess lower or "c" if it is correct. You will agree with me that the user inputs an upper case or lowercase letter, and python is case sensitive, hence the ".casefold()" at the end of the input statement so that it converts all inputs to lowercase, that way you can write your "if statements" with specificity.


```
low = 1
high = 1000
print("Please think of a number between the range {0} and {1}".format(low, high))
input("Press Enter to start")
guesses = 0

while low != high:
    print("\tGuessing in the range of {0} to {1}".format(low, high))
    guess = low + ((high - low) // 2)
    high_low = input("My guess is {}, Should I guess higher or lower? "
                     "Enter h or l or c if I am correct "
                     .format(guess)).casefold()

``` 



Next we write an "if statement". If the user inputs "h" which means to guess higher the lower end of the range becomes the number that was guessed incorrectly by the program plus one. The logic here is that if the number that was guessed was incorrect and the program has to guess higher, then the range should be shortened so that guessing the correct number might be possible. Same thing happens when the user inputs "l" which means to guess lower, then the higher end of the new range becomes the number that was guessed minus one, the same logic happens here too. If the user inputs "c" the program breaks with a message saying it guessed it correctly in "n" number of guesses. The else statement follows and it's function is to check if the user doesn't input any of the letters that were instructed, then it prints out a message for the user to follow the instructions given. The number of guesses increases by 1 every time the program repeats itself. The final number gotten after the program breaks comes out as the number of times the program had to guess to get it correctly


```
low = 1
high = 1000
print("Please think of a number between the range {0} and {1}".format(low, high))
input("Press Enter to start")
guesses = 0

while low != high:
    print("\tGuessing in the range of {0} to {1}".format(low, high))
    guess = low + ((high - low) // 2)
    high_low = input("My guess is {}, Should I guess higher or lower? "
                     "Enter h or l or c if I am correct "
                     .format(guess)).casefold()
    if high_low == "h":
        #Guess higher, the low end of the range becomes the guess + 1
        low = guess + 1
    elif high_low == "l":
        #Guess lower, the high end of the range becomes guess - 1
        high = guess - 1
    elif high_low == "c":
        print("Yay I got it in {} guesses".format(guesses))
        break
    else:
        print("Follow the right instructions, please enter h, l or c")
    guesses += 1

``` 


The "else statement" directly under the "while statement" is for the scenarios when the program has done all possible calculations and it just has to be that number that it brings out. It prints that it got the number you had in mind in "n" number of guesses.


```
low = 1
high = 1000
print("Please think of a number between the range {0} and {1}".format(low, high))
input("Press Enter to start")
guesses = 0

while low != high:
    print("\tGuessing in the range of {0} to {1}".format(low, high))
    guess = low + ((high - low) // 2)
    high_low = input("My guess is {}, Should I guess higher or lower? "
                     "Enter h or l or c if I am correct "
                     .format(guess)).casefold()
    if high_low == "h":
        #Guess higher, the low end of the range becomes the guess + 1
        low = guess + 1
    elif high_low == "l":
        #Guess lower, the high end of the range becomes guess - 1
        high = guess - 1
    elif high_low == "c":
        print("Yay I got it in {} guesses".format(guesses))
        break
    else:
        print("Follow the right instructions, please enter h, l or c")
    guesses += 1
else:
    print("{} is your number isn't it".format(low))
    print("I got in {} guesses".format(guesses))
``` 


And there you have it we have created a simple python game.

Thanks for reading................

Like, Comment and subscribe to my newsletters



