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
