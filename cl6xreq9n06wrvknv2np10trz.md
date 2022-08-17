## Python Loops Explained

In computer science, a loop is a control flow statement for specifying iteration, which allows code to be executed repeatedly.
Python has two types of loops, the " For-Loop" and the "while-loop". A lot of beginners usually find python loops confusing and hard to understand, so I am going to be explaining it using basic knowledge and terminologies.

### The For Loop.

 Python For-Loop can be likened to this example below;
A man has five children, he wants to take them to the mall, buy a book, a pair of shoes, a shirt, and a water bottle for each of them. He wants to take them one at a time and not all at once. if this should be written in code it would look like this


```
for each child in my children:
     Take to the mall
     Buy a book
     Buy a pair of shoes
     Buy a shirt
     Buy a water bottle
``` 
Each of the child in his children get to go to the mall, get a book, a pair of shoes, a shirt and a water bottle. But the way a for loop works, the Father has to take each of the to the mall one after the other.
Likening your codes to your real life situation makes the code easy to read and understand.
Now for a practical Python code example;

```
names = ["peace", "mary", "sarah",  "eleana", "steven", "james"]
for name in names:
    name = name.capitalize()
    print(name)
``` 
What the code directly above does is to capitalize the first letter of each of the names in the list and print each of them. The next example is to calculate the sum of numbers from 1-100 using a for loop

```
result = 0
for num in range(0, 101):
    result += num
print(result)

```
The first line of code is to create a variable to store our result in it, then the for loop. if you noticed, though i wanted the sum of numbers from 1-100, but my upper range limit was 101. This is because when using range, it loops till but not including the last digit of the range, that was why it was needed to add 1 extra. The third line of code is for adding each of the numbers to the result each time the loop runs, and afterwards the next line is for the result to be shown on the console or terminal. The indentation of the last print statement should be moved to the same indent level as the for loop statement, if it is in the loop, it is going to print the addition for each of the step, you could also try that to see how the loop works.

### The While Loop.

Using the same example I used for the for loop, the while loop can be likened to this;
The father just wants to take them to the mall as long as they be of good behavior, more like a condition that has to be fulfilled before they are taken to the mall, and as long as that condition is True the while loop runs. The code is likely to look like this;

```
while child is of good behavior:
       for each child in my children:
           Take to the mall
           Buy a book
           Buy a pair of shoes
           Buy a shirt
           Buy a water bottle
``` 
As we saw above a for loop can be nested in a while loop, and vice-versa. Boo'leans(True/False) can also be used as a conditional statement for a while loop too. Here are some practical Python code examples

```
for i in range(1, 11):
    while i % 2 != 0:
        print(i**2)
        break
``` 
Th is time we are nesting a while loop inside a for loop. We are considering a range of numbers from 1 to 10, 11 is there because of the range up to but not inclusive of the upper range digit. The next line means, while i has a remainder that is not equal to zero when divided by two, print the square of the number. Basically the output will just be the square of all odd numbers from 1 to 10 and the loop breaks afterwards.


Thanks for reading till this point, comment your questions below.




