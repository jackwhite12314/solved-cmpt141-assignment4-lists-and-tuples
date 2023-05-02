Download Link: https://assignmentchef.com/product/solved-cmpt141-assignment4-lists-and-tuples
<br>
<strong>Question 1 </strong>

<strong>Purpose: </strong>To practice your ability to create and manipulate lists.

<strong>Degree of Difficulty: </strong>Easy

Pokemon are fantastic creatures that people like to catch and train. For this question, you will write a program that allows the user to keep track of the Pokemon they have caught, and then assemble a team from among the Pokemon caught that can be taken to the local Pokemon Gym for training.

Your program will have two phases. When the program first starts, it should repeatedly show a prompt to the user asking if they want to catch another Pokemon. Each time they say yes, the program should ask the user to enter the name of the Pokemon that was caught and it should be added to a list variable that holds the user’s complete Pokemon collection. When they say no, the program should continue to the second phase.

Get this part of the program working before going any further. Do not move on to the second part of the program until you know that the first part works.

In the second phase, the program will display the current Pokemon collection, as well as a list of Pokemon that have been added to the user’s Gym Team (initially, this second list will be empty). A prompt will then ask the user to name the Pokemon from their collection that they would like to add to the Gym Team. The Pokemon entered should be removed from the first list (the Pokemon collection) and added to the Gym Team list. This process should continue until EITHER (a) there are 6 Pokemon on the Gym Team, or (b) all of the Pokemon from the collection have already been added to the Gym Team.

<h1>Sample Run</h1>

<table width="652">

 <tbody>

  <tr>

   <td width="652">Time to catch some Pokemon!Which Pokemon have you caught? pikachuWould you like to keep catching Pokemon (y/n)? y So far you’ve caught:[’pikachu’]Which new Pokemon have you caught? wobuffet Would you like to keep catching Pokemon (y/n)? y So far you’ve caught:[’pikachu’, ’wobuffet’]Which new Pokemon have you caught? charmander Would you like to keep catching Pokemon (y/n)? y So far you’ve caught:[’pikachu’, ’wobuffet’, ’charmander’]Which new Pokemon have you caught? bulbasaurWould you like to keep catching Pokemon (y/n)? n~~~Time to head to the Pokemon Gym!~~~Pokemon in your collection:[’pikachu’, ’wobuffet’, ’charmander’, ’bulbasaur’] Pokemon on your Gym Team:[]What Pokemon will you add to your team? pikachu I CHOOSE YOU, PIKACHU!!Pokemon in your collection:[’wobuffet’, ’charmander’, ’bulbasaur’] Pokemon on your Gym Team:[’pikachu’]What Pokemon will you add to your team? wobuffet</td>

  </tr>

 </tbody>

</table>

<table width="652">

 <tbody>

  <tr>

   <td width="652">I CHOOSE YOU, WOBUFFET!!Pokemon in your collection:[’charmander’, ’bulbasaur’] Pokemon on your Gym Team:[’pikachu’, ’wobuffet’]What Pokemon will you add to your team? charmander I CHOOSE YOU, CHARMANDER!!Pokemon in your collection:[’bulbasaur’]Pokemon on your Gym Team:[’pikachu’, ’wobuffet’, ’charmander’]What Pokemon will you add to your team? bulbasaur I CHOOSE YOU, BULBASAUR!! ~~~Your Pokemon team is ready to hit the gym!</td>

  </tr>

 </tbody>

</table>

Here is an example of how your program’s console output might look. Green text was entered by the user.  You may assume that the user will enter correct input in all cases, i.e. the user will only try to add Pokemon  to the Gym Team that are already in the list.

<strong>Question 2 :</strong>

<strong>Purpose: </strong>To practice creating and manipulating lists with list comprehensions.

<strong>Degree of Difficulty: </strong>Mostly Easy

In a4q2-starter.py you are given a definition of a list of lists. Each sublist contains three pieces of information on one famous prairie pirate – their pirate name, the number of sacks of assorted grains they have plundered from unsuspecting farmers in the last year, and a Boolean value indicating whether they like parrots. Create the following list comprehensions where indicated by comments in the provided file a4q2-starter.py. Note that you <strong>only </strong>need to create the appropriate list comprehensions, you do not need to print them out (though you may want to for testing purposes).

<ul>

 <li>Use a single list comprehension to create a <strong>list of strings </strong>of the pirate names who plundered more than 400 sacks of assorted grains.</li>

 <li>Use a single list comprehension to create a <strong>list of strings </strong>of the pirate names who don’t like parrots.</li>

 <li>Suppose that the average market value of a sack of grain is $42. Use a single list comprehension to create a <strong>list of integers </strong>of the market values of each pirate’s grain.</li>

 <li>Use a single list comprehension to create a <strong>list of lists </strong>where each sublist consists of a pirate’s name, and the value of his/her plundered sacks of grain (calculate grain values as in part (c)), but only include those pirates who like parrots.</li>

</ul>

<strong>Question 3 :</strong>

<strong>Purpose: </strong>To practice your ability to modify lists and compute values with lists

<strong>Degree of Difficulty: </strong>Moderate

Professor Oak is in trouble: his class grades are a mess! His midterm exam was too hard, and he gave out too many bonus marks to certain students. For this question, you will write a program to clean up the grades and calculate the final grade for each student in the class. <strong>Starter File</strong>

a4q3_starter.py is a file that contains Professor Oak’s student grades as a list of lists. Each sublist has exactly 6 items, representing the grades for (in order) four assignments, a midterm exam, and a final exam. All grades are out of 100. Just copy/paste this list to the top of your program. But keep in mind that your code should work even if we use a different starting list (though with the same format) to test your program.

From here, you will write three separate functions to perform three tasks, as described below.

<h1>Cleaning the Data</h1>

Write a function called clean_grades() that takes the list of lists of grades as a parameter. For all of the student grades, this function should perform two tasks:

<ul>

 <li>Increase the midterm exam grade for ALL students by 2. Recall that the midterm grade is the 5th item in each sublist.</li>

 <li>For any grade greater than 100, set the grade to be just 100 (make sure to check for this AFTER increasing the grade for the midterm exam!)</li>

</ul>

These changes should be done by modifying the input list itself. No new lists should be created and this function has no return value.

<h1>Student Final Grades</h1>

Write a function called student_averages() that takes the list of lists of grades as a parameter and computes a final grade for each student. The grading scheme for the class is:

<ul>

 <li>10% for each assignment (recall there were 4 assignments)</li>

 <li>20% for the midterm exam</li>

 <li>40% for the final exam</li>

</ul>

The final grade for each student <strong>must be an integer</strong>, rounded appropriately (you can use Python’s round() function for this). The final grades should be placed into a single list and this function must <strong>return </strong>that list.

<h1>Class Average</h1>

Write a function called average() that takes a list of integers representing the grade of each student in the class as a parameter, and <strong>returns </strong>the class average as a single, floating point number.

<h1>Program Output</h1>

At the very bottom of your program, call all of the functions you made above, using their return values appropriately, to print out the list containing each student’s final grade, as well as the overall class average.

<h2>Sample Run</h2>

Here is an example of how your program’s console output might look (the 2nd line will in fact be much




longer; we are showing only the first few numbers here to save space).

The final grades for the class are:

[69, 76, 40, 69, 50, 58, 66, 79, 69, 86, … ]

<table>

 <tbody>

  <tr>

   <td> </td>

  </tr>

 </tbody>

</table>

The overall class average is: 64.04


