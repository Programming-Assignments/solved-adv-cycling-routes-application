Download Link: https://assignmentchef.com/product/solved-adv-cycling-routes-application
<br>
Cycling Routes application

In this assignment you are required to develop a prototype for an application in Scala to extract information from cycling route data. You will be provided with cycling route data, and your application should allow the user to select from the set of options listed below and obtain the results of the chosen selection. The application should have a simple text-based, menu-driven interface.

<h1>Data</h1>

The data is supplied to you as a comma-separated text file <em>cyclingroutedata.txt</em>. Each line of the file contains the route name concatenated with the name of the starting point and 0 or more sets of stage values. Each stage set’s values represent the stage number, the name of the stage endpoint and the length of the stage (in kilometres). A sample line from the file, edited for display purposes, is shown below:

Oor Wullie Route (GCU),1:City

Chambers:0.75,2:Velodrome:3.8,3:People’s Palace:2.7 …

Note the stage values are separated by a colon.

Your application should read the file contents and store the data in a map structure where each line of the file is used to construct a map entry with the route name as the key, and a list of tuples as the value. The type of the structure should be <strong><em>Map[String, List[(Int,String,Float)]]</em></strong>. The sample line shown should be represented within the map as follows:

Map(“Oor Wullie Route (GCU)” -&gt; List((1,City Chambers,0.75), (2,Velodrome,3.8), …))

You will also be supplied with a fragment of Scala code, in a Scala Worksheet file <em>cyclingroutedata.sc, </em>that creates a map with the same format, containing equivalent data. You can use this, if you wish, to test other functions as required without the need to have completed the file reading functionality.

<h1>Options</h1>

Your application should allow the user to perform the following analyses:

<ol>

 <li>Get all the route values and display suitably formatted.</li>

 <li>Get the total distance and number of stages for each route, for all routes</li>

</ol>

e.g. Oor Wullie Route has 6 stages and a total distance of 18.45km

<ol start="3">

 <li>Get the average total distance and average number of stages of all routes.</li>

 <li>Get a report of all routes in descending order of total distance with a summary showing the overall average total distance and overall average number of stages for all routes.</li>

 <li>Get the route details for a user specified route.</li>

 <li>Allow the user to construct a personalised list of routes through selecting one or more routes and adding a comment to each chosen route.</li>

</ol>

<em>Marks for each analysis will be awarded on the basis of completeness and correctness of the implementation.</em>

<h1>Application structure</h1>

The application should be implemented as a Scala singleton object, with the cycling route data map as a field. Your code should firstly read the file data into the map. It should then display a menu, allow the user to input a choice and invoke a suitable handler function for that choice. The menu should have an option for each of the required analyses and also an option to quit the application.

For each analysis it is suggested that you define the following:

<ul>

 <li>A function that performs the required operation on the data and returns the results to be displayed</li>

 <li>A function, to be invoked by a menu option, that accepts user input if required for an operation, invokes the operation function and displays the results of the operation to the user</li>

</ul>

The functions for each analysis should be composed to perform the operation and display the result. For example, the first analysis listed above could be performed using:

<ul>

 <li>A function that is applied to the data and returns a result of type <em>Map[String, (Int,String,Float)] </em></li>

 <li>A function that invokes the operation and iterates through the resulting map to display its contents.</li>

</ul>

Each analysis will differ in terms of the user input required and the type of result returned by the operation.

<em>Marks will be awarded on the basis of completeness and correctness of the implementation, and on producing a well- structured solution. </em>

<h1>Programming style</h1>

Scala doesn’t impose a particular style of programming. However, in this assignment you are encouraged to prefer a functional style over an imperative style wherever possible in your solution. In particular, your solution may demonstrate examples of appropriate use of a range of the following functional programming techniques:

<ul>

 <li>Recursion</li>

 <li>Folding</li>

 <li>Pattern matching</li>

 <li>For comprehensions</li>

 <li>Partial function application</li>

</ul>

<em>Marks will be awarded on the basis of evidence of your ability to implement functional solutions to problems across all aspects of the application.</em>

<h1>Testing</h1>

You should test your operation functions using the test data – for each one you should define input data if required, note the result returned by the function and compare this to the expected result.

You should test your complete application by invoking each menu option using suitable user input and comparing the displayed result with the expected result.

<em>Marks will be awarded on the basis of evidence of a rigorous approach to designing and implementing test cases. </em>

<h1>Evaluation</h1>

You should evaluate the suitability of Scala for developing this application. Your evaluation should refer to language features and the support in the language for the programming approach that you have used in your solution and consider alternative approaches that you could have taken to solve the same problems either using Scala or using a different language that you are familiar with. Your evaluation should be 400-500 words long.

<em>Marks will be awarded for demonstrating an understanding of programming models and their implementation in Scala, related to the requirements of the application.</em>

<h1>Appendix (Oor Wullie Route Details)</h1>

Route Details

<strong><em>Stage 1</em></strong>

GCU to City Chambers – 0.75km

<strong><em>Stage 2</em></strong>

City Chambers to Sir Chris Hoy Velodrome – 3.8km

<strong><em>Stage 3</em></strong>

Sir Chris Hoy Velodrome to People’s Palace – 2.7km

<strong><em>Stage 4</em></strong>

People’s Palace to Riverside Museum – 5.4km

<strong><em>Stage 5</em></strong>

Riverside Museum to Botanic Gardens – 2.4km

<h2>Stage 6</h2>

Botanic Gardens to GCU – 3.4km


