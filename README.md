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
<div class="col-xs-12 col-sm-offset-2 col-sm-8">
<h1 style="color: #b1810b; text-align: left;">HW10 - Challenge</h1>
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
<p>For this Homework, you will be implementing a single class: <code>NumberFinder</code>. This class will process a String input and calculate key statistics.&nbsp;</p>
<p></p>
<p>Note: 5 points of your Challenge grade is based on Coding Style.&nbsp; You will need to follow the standards described <a href="https://purdue.brightspace.com/d2l/le/content/307113/viewContent/6356290/View" target="_blank">here</a>&nbsp;. Use the "Run" button to check your Coding Style without using a submission.&nbsp;</p>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="2">Instructions</h2>
<h3>Here are the assignment requirements:&nbsp;</h3>
<ul>
<li>Create a class that utilizes static variables in a deterministic and multithreaded manner. Your solution must have three static variables:&nbsp;
<ul>
<li>numberCounter: a counter that increments for each number present in the String.</li>
<li>wordCounter: a counter that increments for each valid word present in the String.</li>
<li>total: a variable that tracks the sum of each number present in the String.&nbsp;</li>
</ul>
</li>
<li>The class must be able to be spawned as a Thread.</li>
<li>Objects of the class will be passed a String containing many space-separated words or numbers, a start index (inclusive), and an end index (exclusive).</li>
<li>Within the run() method, the class must iterate through the String from the start index to the end index (but not including the end index) and update the static variables accordingly.&nbsp;</li>
<li>The processing described above should happen concurrently for multiple threads.&nbsp;
<ul>
<li>The only synchronized portions of the solution should be for accessing shared resources.&nbsp;</li>
</ul>
</li>
</ul>
<p></p>
<h3>Class Requirements:&nbsp;</h3>
<h4>Fields</h4>
<table border="1px" style="margin-left: auto; margin-right: auto; width: 666px;">
<tbody>
<tr>
<td style="width: 167.778px;">
<p>Name</p>
</td>
<td style="width: 76.6667px;">
<p>Type</p>
</td>
<td style="width: 170px;">
<p>Access Modifier(s)</p>
</td>
<td style="width: 250px;">
<p>Additional Modifier(s)</p>
</td>
</tr>
<tr>
<td style="width: 167.778px;">
<p>numberCounter</p>
</td>
<td style="width: 76.6667px;">
<p>int</p>
</td>
<td style="width: 170px;">
<p>private</p>
</td>
<td style="width: 250px;">
<p>static</p>
</td>
</tr>
<tr>
<td style="width: 167.778px;">
<p>wordCounter</p>
</td>
<td style="width: 76.6667px;">
<p>int</p>
</td>
<td style="width: 170px;">
<p>private</p>
</td>
<td style="width: 250px;">
<p>static</p>
</td>
</tr>
<tr>
<td style="width: 167.778px;">
<p>total</p>
</td>
<td style="width: 76.6667px;">
<p>double</p>
</td>
<td style="width: 170px;">
<p>private</p>
</td>
<td style="width: 250px;">
<p>static</p>
</td>
</tr>
<tr>
<td style="width: 167.778px;">
<p>start</p>
</td>
<td style="width: 76.6667px;">
<p>int</p>
</td>
<td style="width: 170px;">
<p>private</p>
</td>
<td style="width: 250px;">
<p>N/A</p>
</td>
</tr>
<tr>
<td style="width: 167.778px;">
<p>end</p>
</td>
<td style="width: 76.6667px;">
<p>int</p>
</td>
<td style="width: 170px;">
<p>private</p>
</td>
<td style="width: 250px;">
<p>N/A</p>
</td>
</tr>
<tr>
<td style="width: 167.778px;">
<p>inputText</p>
</td>
<td style="width: 76.6667px;">
<p>String</p>
</td>
<td style="width: 170px;">
<p>private</p>
</td>
<td style="width: 250px;">
<p>N/A</p>
</td>
</tr>
</tbody>
</table>
<p></p>
<h4>Constructors</h4>
<table border="1px" style="margin-left: auto; margin-right: auto; width: 700px;">
<tbody>
<tr>
<td colspan="1" rowspan="1" style="width: 521px;">
<p>Parameters</p>
</td>
<td colspan="1" rowspan="1" style="width: 178px;">
<p>Access Modifier(s)</p>
</td>
</tr>
<tr>
<td colspan="1" rowspan="1" style="width: 521px;">
<p>String inputText, int start, int end</p>
</td>
<td colspan="1" rowspan="1" style="width: 178px;">
<p>public</p>
</td>
</tr>
</tbody>
</table>
<p></p>
<h4>Methods</h4>
<p>You may implement any methods you choose to accomplish the goal, as long as you have a run() method that will process data according to the implementation requirements.&nbsp;</p>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="3">Testing</h2>
<p>No local test cases are provided with this assignment. Instead, we recommend writing your own using the examples we've provided for past assignments.&nbsp;</p>
<p></p>
<p>We will be using the following input String for this testing example:</p>
<p></p>
<p></p>
<pre>String inputText = "This 1 string has nu17mbers in 12 it."</pre>
<p></p>
<p>Say that two NumberFinder Objects are constructed with the following arguments:</p>
<p></p>
<pre>NumberFinder one = new NumberFinder(inputText, 0, 18);<br />NumberFinder two = new NumberFinder(inputText, 18, 37);</pre>
<p></p>
<p>Now, assume that the appropriate method calls take place such that the instantiated NumberFinders are running concurrently. For the sake of example we will describe the logic as occurring linearly, but in reality it will be occurring concurrently.</p>
<p></p>
<p></p>
<p>First, let us look at the NumberFinder named &ldquo;one&rdquo; with start index 0 (inclusive) and end index 18 (exclusive). The corresponding substring of the inputText is &ldquo;This 1 string has &rdquo;. There is one number in this String, along with 3 words. Thus, 1 is added to numberCounter, 3 is added to wordCounter, and the total value of the numbers, 1, is added to total.&nbsp;</p>
<p></p>
<p>Now let us look at the NumberFinder named &ldquo;two&rdquo; with start index 18 (inclusive) and end index 37 (exclusive). The corresponding substring of the inputText is &ldquo;nu17mbers in 12.5 it.&rdquo;. There are two numbers in this String, along with 2 words. Thus, 2 is added to numberCounter, 2 is added to wordCounter, and the total value of the numbers, 29.5, is added to total.&nbsp;</p>
<p></p>
<p>The final values of each field are listed below:&nbsp;</p>
<ul>
<li>numberCounter: 3</li>
<li>wordCounter: 5</li>
<li>total: 30.5</li>
</ul>
<p></p>
<h3>Notes:&nbsp;</h3>
<ul>
<li>You can assume that all start and end indexes will be valid.&nbsp;</li>
<li>If a number appears within a word, "Num10ber", it will count as a number and <strong>NOT</strong> as a word.&nbsp;
<ul>
<li>numberCounter will increment by one, while wordCounter is unmodified.&nbsp;</li>
</ul>
</li>
<li>Numbers may be integers (1) or doubles (12.4).&nbsp;</li>
<li>Any word that does not contain a number is considered valid.&nbsp;</li>
<li>You may assume that two distinct numbers will not appear within a single word, "1test2".&nbsp;
<ul>
<li>Consecutive digits in a single word should be treated as a single number.&nbsp;</li>
<li>For example, "Rand36.5om" is valid while "1n2e3w4" is not.&nbsp;</li>
</ul>
</li>
<li>You do not need to include a main method in your submission, but you should use one during testing.&nbsp;</li>
<li>You should follow the requirements documented in the Debugging handout for preventing race conditions. Solutions that use excessively broad scope are not considered concurrent and will not receive credit.&nbsp;</li>
<li>Remember the difference between static and non-static. As there will be multiple NumberFinder objects, you will need to find a way to implement concurrency among all of them. If your solution does not implement concurrency properly for multiple objects, it will not receive credit.&nbsp;</li>
<li>As long as you implement the requirements specified in this document, you can take any approach to concurrency in your implementation.&nbsp;</li>
</ul>
<h2 id="4">Submit</h2>
<p>After testing your solution and verifying that it meets the requirements described in this document, you can submit on Vocareum. Your work will be manually graded within 7 days of the due date.&nbsp;</p>
</div>
</div>
<footer></footer></main></div>
</body>

</html>
