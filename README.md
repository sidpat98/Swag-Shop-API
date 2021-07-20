<html lang="en">

<head>
	<meta charset="utf-8">
	<meta http-equiv="x-ua-compatible" content="ie=edge">
	<title>Basic Page - No Banner</title>
	<meta name="description" content="">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body class="content layout-2" role="document">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="container-fluid"><main>
<div class="row">
<div class="col-xs-12 col-sm-offset-2 col-sm-8">
<h1 style="color: #b1810b; text-align: left;">HW11 - Challenge</h1>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<p></p>
<ul>
<li><a href="#1">Description</a></li>
<li><a href="#2">Instructions</a></li>
<li><a href="#3" style="background-color: #ffffff;">Testing</a></li>
<li><a href="#4">Submit</a></li>
</ul>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="1">Description</h2>
<p>For this Homework, you will be implementing a GUI application that will perform calculations for the user using Network IO. You will use two classes: CalculatorClient.java and CalculatorServer.java</p>
<p></p>
<p>Note: 5 points of your Challenge grade is based on Coding Style.&nbsp; You will need to follow the standards described <a href="https://purdue.brightspace.com/d2l/le/content/307113/viewContent/6356290/View" target="_blank">here</a>&nbsp;. Use the "Run" button to check your Coding Style without using a submission.&nbsp;</p>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="2">Instructions</h2>
<p>All input and output should be done through <code>JOptionPane</code> dialogs. Any input and output conducted via the terminal will not receive points.&nbsp;</p>
<p></p>
<p><br />The user will be able to enter the host name and port number through a <code>JOptionPane</code>. Once connected, the user can enter an equation and will be given the answer in another <code>JOptionPane</code>.</p>
<p><br />Your application should handle 6 equation types (addition, subtraction, multiplication, division, exponentiation, modulus) and will be formatted as:</p>
<p>[number] [operand] [number]</p>
<p></p>
<p>Note that there must be one space between the first number and the operand and one space between the operand and the second number.</p>
<p><br />The numbers entered by the user should allow for decimals.</p>
<p><br />The following are valid equations:</p>
<ul>
<li>5 + 3</li>
<li>2.7 / 4</li>
<li>3 * 9</li>
<li>-10 - 2.5</li>
<li>4 ^ 2</li>
<li>5 % 2</li>
</ul>
<p>An invalid equation could look like:</p>
<ul>
<li>5</li>
<li>8/4</li>
<li>3 & 9</li>
<li>3 * a</li>
<li>^4</li>
<li>&nbsp;7 - 3 (there are spaces before and after the numbers)</li>
<li>4 -2 (Invalid because there is no space between the '-' and the '2').</li>
</ul>
<p></p>
<p>Note: Calculations should be done on the server.&nbsp;</p>
<h3>Steps</h3>
<p>Your program must perform the following in order:&nbsp;</p>
<ol>
<li>Welcome the user</li>
<li>Prompt the user to enter a host name and port number (you may do this separately or together).
<ol>
<li>If the connection is not established successfully, show an error message and end the program.&nbsp;</li>
</ol>
</li>
<li>Show a connection established message.&nbsp;</li>
<li>Prompt the user to enter their equation.
<ol>
<li>If there is an error in the equation, show an error message and prompt the user to re-enter the equation. Repeat as many times as necessary.&nbsp;</li>
</ol>
</li>
<li>Show the user the result of the calculation.</li>
<li>Ask the user if they wish to enter another equation.
<ol>
<li>If yes, return to step 4.&nbsp;</li>
<li>If no, show a farewell message.&nbsp;</li>
</ol>
</li>
<li>Exit</li>
</ol>
<p></p>
<p>The specifics of the look and feel, the text messages you use, and the types of dialogs are all up to you. Keep in mind that all your decisions should be logical and design oriented.&nbsp;</p>
<p></p>
<p>Hint: Remember, the server needs to be running before you run the client.&nbsp;</p>
<p></p>
<h3>Notes</h3>
<ul>
<li>Your program should handle a situation where the user selects cancel on any option where it is available, or exits the panel.&nbsp;</li>
<li>The client handles user input and displaying the GUI. The server performs the calculations. Solutions that do not organize the implementation appropriately will not receive credit.&nbsp;</li>
<li>The Intellij GUI Designer (or any other shortcut tool) is not allowed for any CS 18000 assignment.&nbsp;
<ul>
<li>If there are .form files in your submission, it will not be graded.&nbsp;</li>
</ul>
</li>
<li>You can choose which port number to use in the Server. Include the number in the client and server class comments.&nbsp;</li>
<li>If the result of the calculation is a double, format it to two decimal places.&nbsp;</li>
<li>Your solution must handle all exceptions and errors.&nbsp;</li>
<li>You will not be able to run your solution on Vocareum. This is expected. As long as you submit, you will be graded.&nbsp;</li>
</ul>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="3">Testing</h2>
<p>Run through the program with sample inputs and verify everything is performing as expected.&nbsp;</p>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="4">Submit</h2>
<p>After testing your solution and verifying that it meets the requirements described in this document, you can submit on Vocareum. Your work will be graded within 7 days of the due date.&nbsp;</p>
<p></p>
</div>
</div>
<footer></footer></main></div>

</body>

</html>
