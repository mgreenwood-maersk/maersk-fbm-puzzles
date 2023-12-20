# AP Moller Maersk - Fulfilled By Maersk Programming Puzzles

In the Maersk FbM platform, our enthusiasm lies in programming puzzles, challenges, and riddles. 

These serve as a key aspect of our recruitment process, as we seek individuals who share our passion for 
tackling complex computing problems with innovative solutions. 

To be eligible for an interview, demonstrate your skills by solving one of the programming puzzles listed 
below and submitting your solution. Check out some helpful tips to kickstart your journey:

* Please use C# or Java to develop your solution, do not use extraneous frameworks in order to solve the problem, your solution should be constrained to your own implementation.
* The implementation should use OOP/SOLID principals.
* Please write your code as 'production ready'
* In your email, along with your source code, please include your program's final answer; a brief (1-2 paragraph) description of your approach and any trade-offs you made
(say, for generality, speed, or ease of implementation); and instructions on how to test your program.
* Please send your puzzle answer and resume to INSERT_EMAIL_ADDRESS_HERE

Puzzle answers will be reviewed only for individuals submitting job applications.
No pseudo-code - pseudo-code will be rejected!

# ASCII A-Maze-ment

Write a program that reads in a simple 2-D maze in a format like these examples:

```
     _______________________FbM
     |     |        |        |
     |__   |_____   |  ______|
     |        |        |     |
     |  ___   |_____   |     |
     |  |  |           |  |  |
     |  |  |  ___      |  |  |
     |  |        |  |  |  |  |
     |  |_____   |__|__|__|  |
     |  |                    |
Start|__|____________________|

      ______________FbM
     |              |
     |________   ___|
     |        |     |
     |  ___   |     |
     |  |        |  |
     |  |__   ___|  |
     |  |     |     |
Start|__|_____|_____|

      _________________FbM
     |                 |
     |__   ______   ___|
     |     |        |  |
     |_____|  ______|  |
     |              |  |
     |__   ___   ___|  |
     |     |  |  |     |
     |_____|  |  |  ___|
     |  |  |           |
     |  |  |__         |
     |           |  |  |
Start|___________|__|__|

```
Download the mazes above as ASCII text. [sample-mazes.txt](sample-mazes.txt)

The input is guaranteed to be a well-formed maze and to have a unique solution path from the bottom left 
grid cell to the top right grid cell. 
Your program should re-output the maze with the solution path filled in, e.g.:

```
      _______________________FbM
     |     |        |XX XX XX|
     |__   |_____   |  ______|
     |XX XX XX|      XX|     |
     |  ___   |_____   |     |
     |XX|  |XX XX XX XX|  |  |
     |  |  |  ___      |  |  |
     |XX|        |  |  |  |  |
     |  |_____   |__|__|__|  |
     |XX|                    |
Start|__|____________________|

      ______________FbM
     |         XX XX|
     |________   ___|
     |XX XX XX|XX   |
     |  ___   |     |
     |XX|   XX XX|  |
     |  |__   ___|  |
     |XX|     |     |
Start|__|_____|_____|

      _________________FbM
     |            XX XX|
     |__   ______   ___|
     |     |XX XX XX|  |
     |_____|  ______|  |
     |      XX XX   |  |
     |__   ___   ___|  |
     |     |  |XX|     |
     |_____|  |  |  ___|
     |  |  |   XX      |
     |  |  |__         |
     |XX XX XX XX|  |  |
Start|___________|__|__|
```

# Instance Search

Write a .NET C# console application which provides "instant search" over properties listed in the National Register of Historic Places.
Rather than waiting for the user to hit return, your application will dynamically update search results as input is typed. We provide 
the file [nrhp.xml.gz](nrhp.xml.gz), which contains selected information from the register's database.

Database The key component of your server-side application is an efficient, in-memory data structure for looking up properties 
(written in pure C#). A good solution may take several minutes to load, but can answer a query in well under 0.1 ms on a modern PC. 

(Note that a sequential search of all properties is probably too slow!) An input matches a property if it is found at any position 
within that property's names, address, or city+state. Matches are case-insensitive, and consider only the characters A-Z and 0-9, e.g. 
the input "mainst" matches "200 S Main St" and "red" matches "Lakeshore Dr." Note that the server's C# will be configured with 
1024M maximum heap space. Please conform to the interfaces specified in nrhp.jar when creating your database.

## Extra Credit

Write the application as a web application - your controller should accept an input string as the request parameter to a GET request. 
Results should include the information for a pre-configured number of properties (e.g. 10), the total number of matches which exist 
in the database, and the time taken by your search algorithm. Your servlet should be stateless, ie. not depend on any per-user session
information. Paginate your additional results as a bonus!

Client Your web page should access the servlet using JavaScript's XMLHttpRequest object. As the user types, your interface should 
repeatedly refine the list of search results without refreshing the page.

Please submit a runnable .NET application, configuration instructions, your source code, and any comments on your approach. 

![image](https://github.com/Maersk-Global/fbm-software-interview/assets/140083932/619aa65c-f1bc-4945-a93a-c9024123266a)


# Palindromic Pangram

A palindrome is a sequence of words like "lid off a daffodil" or "shallot ayatollahs" that uses the same letters 
reading backwards as forwards. The words need not form a meaningful or grammatical sentence.

A palindromic pangram is a multi-word palindrome that includes all 26 letters of the alphabet. Find the 
shortest sequence of words that is both a pangram and a palindrome. Use this dictionary: [WORD.LST](WORD.LST)

# Sling Blade Runner

How long a chain of overlapping movie titles, like Sling Blade Runner, can you find?

Use the following listing of movie titles: [MOVIES.TXT](movies.txt). Multi-word overlaps, as in 
"License to Kill a Mockingbird," are allowed. The same title may not be used more than 
once in a solution. Heuristic solutions that may not always produce the greatest number
of titles will be accepted: seek a reasonable tradeoff of efficiency and optimality.

Data provided by MovieLens at the University of Minnesota.
