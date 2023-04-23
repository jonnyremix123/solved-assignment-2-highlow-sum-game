Download Link: https://assignmentchef.com/product/solved-assignment-2-highlow-sum-game
<br>
<ol>

 <li><strong> Overview </strong></li>

</ol>

This assignment aims to establish a basic familiarity with the JDK development system and its associated on-line Java API class documentation. Students should apply the appropriate fundamental programming concepts (such as variables, constants, arrays, strings, methods, selection and repetition constructs etc.) and make use of appropriate Java API classes (such as Scanner, PrintWriter, String etc.) that they have learnt to solve the given problem.




<ol start="2">

 <li><strong> Objectives </strong></li>

</ol>

On completion of this assignment a student should be able to write simple Java application

that:

<ul>

 <li>Makes use of selection and repetition constructs to achieve desired outcomes</li>

 <li>Stores data to and reads data from arrays</li>

 <li>Generates output to and reads input from the console window</li>

 <li>Reads data from and writes data to text file</li>

 <li>Manipulates string using Java API “String” class</li>

 <li>handles basic errors</li>

 <li>Applies object-oriented concepts</li>

</ul>




<ol start="3">

 <li><strong> Scope </strong></li>

</ol>

This assignment is based on individual effort. You are required to design, develop and test a one player Java game application named “HighLow Sum”.

Besides providing the required functionalities, your program should incorporate appropriate error handling. Comments are also to be inserted to improve program clarity. Before you start coding your program, you are strongly advised to carry out proper problem analysis and program design.  You are required to use JDK 1.5 developer version or later.




<ol start="4">

 <li><strong> Requirements</strong></li>

</ol>

<strong> </strong><strong>4.1 Background</strong>

HighSum is a turned based community card game that can be played with two to five players.

One of the players will be the dealer.

In this assignment, there is only 1 dealer, that is the Java program, and a single human player.

The game uses a standard deck of 52 French playing cards.

A standard deck of 52 French cards consist of four suite; clubs (&#x2663;), diamonds (&#x2666;), hearts (&#x2665;) and spades (&#x2660;). Each suite consists of 13 cards with the following symbol; A,2,3,4,5,6,7,8,9,10,J,Q, K.

Since the dealer is “a type” of player, references to “player” may be to the dealer or the single human player.

<u>Values of Cards</u>

The game uses one or more decks of the standard playing cards.

The suits are ranked as below

<ul>

 <li>spades (highest).</li>

 <li>hearts,</li>

 <li>clubs,</li>

 <li>diamonds (lowest)</li>

</ul>

The red cards (hearts and diamonds) are valued as follows:

<ul>

 <li>Cards from 1 (Ace) through 9 are valued at their face value.</li>

 <li>The 10, Jack, Queen, and King are all valued at 10.</li>

</ul>

The black cards (spades and clubs) are valued as follows:

<ul>

 <li>Cards from 1 (Ace) through 9 are valued at <u>negative of their face value</u>.</li>

 <li>The 10, Jack, Queen, and King are all valued at <u>-10</u>.</li>

</ul>

The value on a player hand is the sum of the point counts of each card in the hand.

For example, a hand containing (4,-6,9) has the value of 7.

<u>Game Procedure</u>

<u>Game Start</u>

The game starts with the dealer shuffles the deck of cards.

The dealer will deal (distribute) the cards to the players.

The dealer make two passes so that the players and the dealer have two cards each.

Two passes means that the dealer must distribute the cards in such a way that, the first card belongs to the player, the second card belongs to the dealer, the third card belongs to the player and the fourth card belows to the dealer.

<u>Round 1</u>

The first card of the dealer and player are both hidden, that is face down.

The dealer and player can view their own hidden first card.

The second card is visible to both the dealer and player.

The player with the highest second card surface value will make a “call” by stating the amount to bet.  The other player will need to place the same amount of bet.

If two cards have the same surface value, use suits ranking to break the tie.

Both the bet amount from dealer and player will be placed on the table.

The dealer is not allowed to quit the game.

<u>Round 2 </u>

The dealer make one pass.

Dealer and player each have 3 cards now.




The player with the highest third card surface value will make a “call” by stating the amount to bet.

The other player will need to place the same amount of bet or choose to quit the current game.




If the human player choose to quit at this round, all the chips on the table belongs to the dealer and the current game ends here.

Both the bet amount from dealer and player will be placed on the table.

The dealer is not allowed to quit the game.

<u>Round 3 </u>

Similar to round 2.

<u>Round 4</u>

Similar to round 2 plus the following rule:




Each player compares the values of cards hold by other players at the end of each game to determine the winner. The player with the highest accumulate value wins the game.

The winner gets all the bet on the table.

If two players get the same highest accumulate value, the bet on the table is shared by both players.




<u>Next Game</u>

All the cards on the table are shuffled and placed at the end of the deck.

The game will start again unless the player choose to leave the game.




<strong>4.2 Minimum required </strong><strong>Functionalities</strong>




Develop a Java program for the <u>two-players</u> HighLow Sum game described above.




The game starts by the player logging into the game. The players’ data (login in, SHA-256 password, last login date and score) are stored in players.dat file from assignment 1.

(The texts in <strong>bold</strong> are data input by the player)




HIGHLOW SUM GAME LOGIN

——————————————————————————–

Enter Login name&gt; <strong>IcePeak</strong>

Enter Password &gt; <strong>password</strong>




Upon logging in, the player will enter the game.

(Below is a sample output of one game play)




HIGHLOW SUM GAME

================================================================================

IcePeak, You have 100 chips

——————————————————————————–

Game starts – Dealer shuffles deck.

——————————————————————————–

Dealer dealing cards – ROUND 1

——————————————————————————–

Dealer

&lt;HIDDEN CARD&gt; &lt;Club 6 (-6)&gt;

Partial Value: -6




IcePeak

&lt;Diamond Ace(+1)&gt; &lt;Spade 6(-6)&gt;

Value:-5

<strong> </strong>

Player call, state bet: <strong>10</strong>

IcePeak, You are left with 90 chips

Bet on table : 20

——————————————————————————–

Dealer dealing cards – ROUND 2

——————————————————————————–

Dealer

&lt;HIDDEN CARD&gt; &lt;Club 6 (-6)&gt; &lt;Diamond 9 (+9)&gt;

Partial Value: 3




IcePeak

&lt;Diamond Ace(+1)&gt; &lt;Spade 6(-6)&gt; &lt;Heart 7(+7)&gt;

Value:2

<strong> </strong>

Dealer call, state bet: 10

Do you want to follow? [Y/N]:<strong> Y</strong>

IcePeak, You are left with 80 chips

Bet on table : 40

——————————————————————————–

Dealer dealing cards – ROUND 3

——————————————————————————–

Dealer

&lt;HIDDEN CARD&gt; &lt;Club 6 (-6)&gt; &lt;Diamond 9 (+9)&gt; &lt;Heart Ace (+1)&gt;

Partial Value: 4




IcePeak

&lt;Diamond Ace(+1)&gt; &lt;Spade 6(-6)&gt; &lt;Heart 7(+7)&gt; &lt;Spade 9 (-9)&gt;

Value:-7

<strong> </strong>

Do you want to [C]all or [Q]uit?:<strong> C</strong>

Player call, state bet: <strong>10</strong>

You are left with 70 chips

Bet on table : 60

——————————————————————————–

Dealer dealing cards – ROUND 4

——————————————————————————–

Dealer

&lt;HIDDEN CARD&gt; &lt;Club 6 (-6)&gt; &lt;Diamond 9 (+9)&gt; &lt;Heart Ace (+1)&gt; &lt;Spade 2 (-2)&gt;

Partial Value: 2




IcePeak

&lt;Diamond Ace(+1)&gt; &lt;Spade 6(-6)&gt; &lt;Heart 7(+7)&gt; &lt;Spade 9 (-9)&gt; &lt;Heart King (+10)&gt;

Value    : 3

<strong> </strong>

Do you want to [C]all or [Q]uit?:<strong> C</strong>

Player call, state bet: <strong>10</strong>

You are left with 60 chips

Bet on table : 80

——————————————————————————–

Game End – Dealer reveal hidden cards

——————————————————————————–

Dealer

&lt;Spade Ace (-1)&gt; &lt;Club 6 (-6)&gt; &lt;Diamond 9 (+9)&gt; &lt;Heart Ace (+1)&gt; &lt;Spade 2 (-2)&gt;

Value: 1




IcePeak

&lt;Diamond Ace&gt; &lt;Spade 6&gt; &lt;Heart 7&gt; &lt;Spade 9&gt; &lt;Heart King&gt;

Value    : 3




IcePeak Wins

IcePeak, You have 140 chips

Dealer shuffles used cards and place behind the deck.

——————————————————————————–

Next Game? (Y/N) &gt;<strong> Y</strong>




And the game continues until the player exits the game.




<strong> </strong>

<strong>Updates of player’s score</strong>




After each game, the program should update the score for that player in the players.dat text file immediately.

For example if IcePeak old chip is 100 and IcePeak wins the current game, the file should be updated to:




For example

<table>

 <tbody>

  <tr>

   <td width="686">BlackRanger|21a57f2fe765e1ae4a8bf15d73fc1bf2a533f547f2343d12a499d45643453ad4|10|Jason Tan|<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="256f71656676666c1714160b464a48">[email protected]</a>|2000-1-18BlueKnight|e765e4456e4f1ae4ae8bf15d73f435535e4a56f441f2556315a23646473e3454|15|Mary Tey|<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e3aeb7a3a0b0a0aad1d2d0cd808c8e">[email protected]</a>|1999-2-22IcePeak|343a4d56b453c76e5e1ae54a8bf15d73fc1bf2a533f547f2343d19c0592044d4|<strong>140</strong>|Peter Loh|<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="faaaaebab9a9b9b3c8cbc9d4999597">[email protected]</a>|1998-1-9GoldDigger|bf2a536446464643e32335b3eddff2233433f547f2343d12a49343345ab53c4d|22|Zack Toh|<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="82d8d6c2c1d1c1cbb0b3b1ace1edef">[email protected]</a>|2001-3-8</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Error Handling</strong>

<strong> </strong>

Your program should be able to handle error situations like where a player enter wrong password. You should look out for other possible exceptions and handle them too.




<ol start="5">

 <li><strong> Submission </strong></li>

</ol>

A complete submission requires the following items:




<ul>

 <li>Report</li>

 <li>Program in Zip file for execution (see below)</li>

 <li>Merge all your class codes (exclude the Utility, Keyboard, Card and Deck class) into a single txt file for turnitin submission. (see below)</li>

</ul>




<u>Zip file instruction</u>

Go to the Eclipse workspace folder, locate your project folder and then the src folder.

Copy all the dat files into the src folder (or the appropriate subfolders).

Make sure that you are able to compile and run your program using the command (<strong><em>javac GameModule.java </em></strong>and<strong><em> java GameModule</em></strong>) directly from the command prompt from the project src folder.

Rename the project src folder using your UoW student number.

Zip up the folder for submission.




As I might be running and testing your codes from my laptop, it is very crucial that you follow the above instruction for submission.




<u>Merge all java class codes using SignAllFiles</u>

Download SignAllFiles.class from Moodle.

Copy SignAllFiles.class into the project folder.

Remove the common Utility,Keyboard, Card and Deck class from the project folder.

From the command line, change directory to the project folder.

Run “java SignAllFiles”

A txt file with the all the java codes name will be generated.

The text file is named with a hash value (digital signature).

Do not rename the file, the digital signature is a prove that the codes you submit in the zip file and the codes for turnitin check is exactly the same.

Submit that generated txt file to Moodle for turnitin check.




Note: You need to ensure that the files you have submitted in the zip files and the merged files (with digital signature) are exactly the same.




Missing in any of the above items is consider non-submission.

Late submission for any above items is consider late submission.




<strong>Program file header </strong>

For each Java program file, provide the header as shown

/*

* CSCI213 Assignment 2

* ————————–

* File name: (state name of .java file)

* Author: (State student name in FULL)

* Student Number: (State UOW student number)

* Description: (A brief description of this class)

*/













Any late submission of work must be accompanied by an application for Special Consideration, requested via SOLS. Unless an extension is granted, any late submission will receive a penalty of 25% of its total worth per day including weekends, and will result in zero mark being recorded on or after the 3<sup>rd</sup> late day. Request for extension with supporting document must be submitted to SIM administration for further consideration before the submission date and the tutor must be informed. Extension will be granted on a case-by-case basis.

<strong> </strong>

<strong>Report requirements</strong>

The report to be submitted consists of the following sections:

<ol>

 <li>Cover page – clearly state your name and UOW student’s number.</li>

 <li>Content Page</li>

 <li>UML class design</li>

 <li>Test-run of Program: You have to provide screen outputs to show the correct execution of your program according to the requirements stated.</li>

 <li>Error Handling: List down and explain the errors and exceptions that your program can handle. Provide screen captures here.</li>

 <li>Enhancements: List down and explain all the enhancements that your have done. Provide screen captures here</li>

 <li>Conclusion and Reflection</li>

</ol>

<strong> </strong>

<strong>Testing requirements</strong>

Make sure that you are able to compile and run your program using the command (<strong><em>javac GameModule.java </em></strong>and<strong><em> java GameModule</em></strong>) directly from the command prompt from the project src folder.




In the players.dat, you should have the following FOUR players’ data.




<table>

 <tbody>

  <tr>

   <td width="98">Login Name</td>

   <td width="91">Password</td>

   <td width="51">Chips</td>

   <td width="76">Name</td>

   <td width="109">E mail</td>

   <td width="95">Birthdate</td>

  </tr>

  <tr>

   <td width="98">p1</td>

   <td width="91">p1</td>

   <td width="51">10</td>

   <td width="76">Player 1</td>

   <td width="109"><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="b2e283f2f1e1f1fb8083819cd1dddf">[email protected]</a></td>

   <td width="95">2000-1-11</td>

  </tr>

  <tr>

   <td width="98">p2</td>

   <td width="91">p2</td>

   <td width="51">12</td>

   <td width="76">Player 2</td>

   <td width="109"><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="267614666575656f1417150845494b">[email protected]</a></td>

   <td width="95">2001-12-2</td>

  </tr>

  <tr>

   <td width="98">p3</td>

   <td width="91">p3</td>

   <td width="51">15</td>

   <td width="76">Player 3</td>

   <td width="109"><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="adfd9eedeefeeee49f9c9e83cec2c0">[email protected]</a></td>

   <td width="95">1999-2-7</td>

  </tr>

  <tr>

   <td width="98">p4</td>

   <td width="91">p4</td>

   <td width="51">9</td>

   <td width="76">Player 4</td>

   <td width="109"><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="88d8bcc8cbdbcbc1bab9bba6ebe7e5">[email protected]</a></td>

   <td width="95">1998-3-15</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

Refer to Report guideline and marks allocation document for detailed report requirements.


