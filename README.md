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
<div class="col-xs-12 col-sm-offset-2 col-sm-8">
<h1 style="color: #b1810b; text-align: left;">PJ03 - Handout</h1>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<p></p>
<ul>
<li><a href="#1">Description</a></li>
<li><a href="#5">Reversi Rules&nbsp;</a></li>
<li><a href="#2">Instructions</a></li>
<li><a href="#3" style="background-color: #ffffff;">Testing</a></li>
<li><a href="#4">Submit</a></li>
</ul>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="1">Description</h2>
<p>For this project, you will be writing an implementation of the game Reversi. While we will be calling the game Reversi, we will actually be using the rules from the version of the game known as Othello.&nbsp;</p>
<p>This project is worth 10% of your final grade. We recommend that you take it, along with the other projects in the class, very seriously. </p>
<p>This game is played between two players, with one player using black pieces and the other player using white pieces. The players take turns setting their pieces on an 8x8 game board. The goal of the game is to have the most pieces on the board by the end. More detailed rules and instructions are in their own section below.&nbsp;</p>
<p></p>
<p>Note: For this assignment, we will only grade your overall implementation. We provide details on methods included in the Starter Code to help you, but you may modify these if you like. More details are included below.&nbsp;</p>
<p></p>
<p>There are three classes in the Starter Code: <code>Point</code>, <code>Reversi</code>, and <code>Game</code>.</p>
<ul>
<li><code>Point</code>&nbsp;is a class that represents the location of a piece on the 2-dimensional game board. You do not need to make any changes to this class.</li>
<li><code>Reversi</code>&nbsp;is a class that launches the game and handles the logistics of game delivery and management. You will need to complete the methods marked "TODO".</li>
<li><code>Game</code>&nbsp;is a class that handles the specific game mechanics and rules associated with Reversi. You will need to complete the methods marked "TODO".</li>
</ul>
<p></p>
<p>You will not need to implement any additional classes beyond the ones described above, though you may do so if you wish.&nbsp;</p>
<p></p>
<p>Note: 5 points of your grade is based on Coding Style.&nbsp; You will need to update the Starter Code to follow the standards described <a href="https://purdue.brightspace.com/d2l/le/content/307113/viewContent/6356290/View" target="_blank">here</a>&nbsp; Use the "Run" button to check your Coding Style without using a submission.&nbsp;</p>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="5">Reversi Rules</h2>
<p>The game rules are explained in subsections below. All output examples are formatted in the same way the game board will be printed by the program.&nbsp;</p>
<h3>Setup &amp; Moves</h3>
<p>The gameboard is initially set with 4 pieces in the center, 2 white pieces and 2 black pieces. The pieces are arranged in a square and alternate by color in each row. The player using black pieces places the first piece after the board is initialized. Our game will always indicate the available moves for a player by printing an "*" in spaces where a move would be legal.&nbsp;</p>
<pre>  1 2 3 4 5 6 7 8<br />1 _ _ _ _ _ _ _ _<br />2 _ _ _ _ _ _ _ _<br />3 _ _ _ * _ _ _ _<br />4 _ _ * W B _ _ _<br />5 _ _ _ B W * _ _<br />6 _ _ _ _ * _ _ _<br />7 _ _ _ _ _ _ _ _<br />8 _ _ _ _ _ _ _ _</pre>
<p>Players alternate turns placing their pieces in positions such that there exists at least one straight (horizontal, vertical, or diagonal) occupied line between the new piece and another old piece of the same color, adjacent to one or more pieces of the other color. In the example above, all the positions marked with an "*" are points at which a black piece could be placed.</p>
<p></p>
<p>For example, the "*" in location 3,4 (row 3, column 4) is valid because that makes a diagonal line with the "B" in 4,5 and it is adjacent to the "W" in 4,4. A "*" in 3,6 would make a vertical line with the "B" in 4,5, but would not be adjacent to any "W".</p>
<h3>Gameplay</h3>
<p>When a piece is placed on the board, all the pieces the opposing player placed that are between the new piece and the old piece are flipped to the opposite color.&nbsp;</p>
<p></p>
<p>For the purposes of this project, players will indicate their moves by entering an integer number that corresponds to a row and column on the game board. If the user enters 43, then the row is 4 and the column is 3.&nbsp;</p>
<p></p>
<p>For example, given an initial gameboard:&nbsp;</p>
<pre>  1 2 3 4 5 6 7 8<br />1 _ _ _ _ _ _ _ _<br />2 _ _ _ _ _ _ _ _<br />3 _ _ _ * _ _ _ _<br />4 _ _ * W B _ _ _<br />5 _ _ _ B W * _ _<br />6 _ _ _ _ * _ _ _<br />7 _ _ _ _ _ _ _ _<br />8 _ _ _ _ _ _ _ _</pre>
<p>If the first move were to place a piece at position 43 (that is, row 4, column 3 as indicated above), the new board would be as follows:</p>
<pre>  1 2 3 4 5 6 7 8<br />1 _ _ _ _ _ _ _ _<br />2 _ _ _ _ _ _ _ _<br />3 _ _ * _ * _ _ _<br />4 _ _ B B B _ _ _<br />5 _ _ * B W _ _ _<br />6 _ _ _ _ _ _ _ _<br />7 _ _ _ _ _ _ _ _<br />8 _ _ _ _ _ _ _ _</pre>
<p>The white piece that was between the new black piece at 43 and the old black piece at 45 is now counted towards the total number of black pieces on the board.&nbsp;</p>
<p></p>
<p>Note: Notice that the list of available moves changes to the next player after any valid move is made.&nbsp;</p>
<p></p>
<p>Now, consider the board after the second player places a piece at 33.&nbsp;</p>
<pre>  1 2 3 4 5 6 7 8<br />1 _ _ _ _ _ _ _ _<br />2 _ _ * _ _ _ _ _<br />3 _ _ W * _ _ _ _<br />4 _ _ B W B _ _ _<br />5 _ _ _ B W * _ _<br />6 _ _ _ _ * _ _ _<br />7 _ _ _ _ _ _ _ _<br />8 _ _ _ _ _ _ _ _</pre>
<p>Pieces can be flipped to either player after every move. As the game progresses, the number of pieces being changed on any given move will increase.&nbsp;</p>
<h3>Win Conditions</h3>
<p>If one player can not make a valid move, their turn is skipped automatically. When neither player can move, the game ends.</p>
<p></p>
<p>The game will end when one of the following is true:</p>
<ul>
<li>The entire game board (all 64 potential positions) is full.&nbsp;</li>
<li>Neither player has any legal moves remaining.&nbsp;</li>
<li>One player has no pieces remaining on the board.&nbsp;</li>
</ul>
<p></p>
<p>The player with the most remaining pieces at the end of the game is the winner.&nbsp;</p>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="2">Instructions</h2>
<p>Note: For this project, we will only be testing your overall implementation. We provide the suggested methods as guidance to help you implement a solution. As long as your Reversi class has a main method that allows the game to be played and meets the specifications (while following all the rules and output expectations described in this document), you can customize your solution as you like. </p>
<p></p>
<p>Review the <code>Point</code>&nbsp;class for use in your implementation.&nbsp;</p>
<h3 dir="auto"><span style="color: #c7254e; font-family: Menlo, Monaco, Consolas, Courier New, monospace;"><span style="font-size: 18px; background-color: #bfe6ff;">Game</span></span>&nbsp;class</h3>
<p>Finish implementing the <code>Game</code>&nbsp;class using the specifications below.&nbsp;&nbsp;</p>
<h4 dir="auto"><a id="user-content-fields" href="#fields" aria-hidden="true"></a>Fields</h4>
<table dir="auto" style="height: 150px; width: 767px;" border="1px">
<tbody>
<tr style="height: 18px;">
<th style="height: 18px; width: 72.2222px;">Name</th>
<th style="height: 18px; width: 70px;">Type</th>
<th style="height: 18px; width: 143.333px;">Modifier</th>
<th style="width: 480px; height: 18px;">Description</th>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 72.2222px;"><code>point</code></td>
<td style="height: 20px; width: 70px;"><code>Point</code></td>
<td style="height: 20px; width: 143.333px;"><code>public</code></td>
<td style="width: 480px; height: 20px;">An individual point on the game board.&nbsp;</td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 72.2222px;"><code>board</code></td>
<td style="height: 20px; width: 70px;"><code>char[][]</code></td>
<td style="height: 20px; width: 143.333px;"><code>private final</code></td>
<td style="width: 480px; height: 20px;">The game board.&nbsp;</td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 72.2222px;"><code>wScore</code></td>
<td style="height: 20px; width: 70px;"><code>int</code></td>
<td style="height: 20px; width: 143.333px;"><code>public</code></td>
<td style="width: 480px; height: 20px;">The current number of white pieces on the board.</td>
</tr>
<tr style="height: 54px;">
<td style="width: 72.2222px; height: 54px;"><code>bScore</code></td>
<td style="width: 70px; height: 54px;"><code>int</code></td>
<td style="width: 143.333px; height: 54px;"><code>public</code></td>
<td style="width: 480px; height: 54px;">The current number of black pieces on the board.</td>
</tr>
<tr style="height: 18px;">
<td style="width: 72.2222px; height: 18px;"><code>remaining</code></td>
<td style="width: 70px; height: 18px;"><code>int</code></td>
<td style="width: 143.333px; height: 18px;"><code>public</code></td>
<td style="width: 480px; height: 18px;">The number of open points on the game board remaining.</td>
</tr>
<tr>
<td style="width: 72.2222px;"><code>boardX</code></td>
<td style="width: 70px;"><code>char[]</code></td>
<td style="width: 143.333px;"><code>private final</code></td>
<td style="width: 480px;">The labels for each side of the game board.&nbsp;</td>
</tr>
</tbody>
</table>
<h4 dir="auto"></h4>
<h4 dir="auto"><a id="user-content-constructor" href="#constructor" aria-hidden="true"></a>Constructor</h4>
<table dir="auto" border="1px" style="width: 768px;">
<tbody>
<tr>
<th style="width: 365.556px;">Parameters (order matters)</th>
<th style="width: 401.111px;">Modifier</th>
</tr>
<tr>
<td style="width: 365.556px;">None</td>
<td style="width: 401.111px;"><code>public</code></td>
</tr>
</tbody>
</table>
<h4 dir="auto"><a id="user-content-methods-1" href="#methods-1" aria-hidden="true"></a>Methods</h4>
<table dir="auto" style="height: 154px; width: 770px;" border="1pz">
<tbody>
<tr style="height: 36px;">
<th style="height: 34px; width: 227.778px;">Name</th>
<th style="height: 34px; width: 78.8889px;">Return Type</th>
<th style="height: 34px; width: 462.222px;">Parameters</th>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 227.778px;"><code>displayBoard</code></td>
<td style="height: 20px; width: 78.8889px;"><code>void</code></td>
<td style="height: 20px; width: 462.222px;">None</td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 227.778px;"><code>gameResult</code></td>
<td style="height: 20px; width: 78.8889px;"><code>int</code></td>
<td style="height: 20px; width: 462.222px;"><code>Point[] validWhiteLocations, Point[] validBlackLocations</code></td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 227.778px;"><code>getPlaceableLocations</code></td>
<td style="height: 20px; width: 78.8889px;"><code>Point[]</code></td>
<td style="height: 20px; width: 462.222px;"><code>char player, char opponent</code></td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 227.778px;"><code>showPlaceableLocations</code></td>
<td style="height: 20px; width: 78.8889px;"><code>void</code></td>
<td style="height: 20px; width: 462.222px;"><code>Point[] locations, char player, char opponent</code></td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 227.778px;"><code>placeMove</code></td>
<td style="height: 20px; width: 78.8889px;"><code>void</code></td>
<td style="height: 20px; width: 462.222px;"><code>Point point, char player, char opponent </code></td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 227.778px;"><code>updateScores</code></td>
<td style="height: 20px; width: 78.8889px;"><code>void</code></td>
<td style="height: 20px; width: 462.222px;">None</td>
</tr>
</tbody>
</table>
</div>
<div class="col-xs-12 col-sm-offset-2 col-sm-8"></div>
<div class="col-xs-12 col-sm-offset-2 col-sm-8">
<p></p>
<ul>
<li><code>displayBoard</code> <br />
<ul>
<li>Displays the current game board.&nbsp;</li>
</ul>
</li>
<li><code>gameResult</code> <br />
<ul>
<li>Calculate and return the result of the game.&nbsp;
<ul>
<li>Cases:
<ul>
<li>Return 1 - There are more black pieces than white pieces.</li>
<li>Return 0 - There are an equal number of black pieces and white pieces.</li>
<li>Return -1 - There are more white pieces than black pieces.&nbsp;</li>
</ul>
</li>
</ul>
</li>
</ul>
</li>
<li><code>getPlaceableLocations</code> <br />
<ul>
<li>This method checks which points are valid moves for the current player. Then, it returns an array of those positions.</li>
<li>There are only 64 positions in our 8x8 board, so 64 is the upper limit.</li>
<li>8 cases need to be checked: top down, bottom up, left to right, right to left and the 4 diagonals.</li>
</ul>
</li>
<li><code>showPlaceableLocations</code> <br />
<ul>
<li>Places a '*' in the game board at every valid position the current player can place a piece.&nbsp;</li>
</ul>
</li>
<li><code>placeMove</code> <br />
<ul>
<li>Updates the board with the results of the current player making a move.&nbsp;</li>
</ul>
</li>
<li><code>updateScores</code> <br />
<ul>
<li>Updates the scores of both players after every move.&nbsp;</li>
<li>Scores refer to the number of pieces each player has on the board.&nbsp;</li>
</ul>
</li>
</ul>
</div>
<h3 class="col-xs-12 col-sm-offset-2 col-sm-8"><code style="font-weight: bold; letter-spacing: 0.2px;">Reversi</code><span style="font-family: inherit; font-size: 1rem; font-weight: bold; letter-spacing: 0.2px;"> class</span></h3>
<ul></ul>
<div class="col-xs-12 col-sm-offset-2 col-sm-8">
<p dir="auto">Finish implementing the <span style="font-family: inherit; font-size: 1rem; letter-spacing: 0.2px;"><code style="font-weight: bold; letter-spacing: 0.2px;">Reversi</code> </span> class using the specifications below.&nbsp;</p>
<p dir="auto">All the print statements you will need are included as comments.&nbsp;</p>
<h4 dir="auto"><a id="user-content-methods-1" href="#methods-1" aria-hidden="true"></a>Methods</h4>
<p>Note: All methods in this class are <code>public</code> and <code>static</code>.</p>
<table dir="auto" style="height: 118px; width: 613px;" border="1pz">
<tbody>
<tr style="height: 36px;">
<th style="height: 38px; width: 200px;">Name</th>
<th style="height: 38px; width: 78.8889px;">Return Type</th>
<th style="height: 38px; width: 332.222px;">Parameters</th>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 200px;"><code>isFull</code></td>
<td style="height: 20px; width: 78.8889px;"><code>boolean</code></td>
<td style="height: 20px; width: 332.222px;"><code>Point[] board</code></td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 200px;"><code>contains</code></td>
<td style="height: 20px; width: 78.8889px;"><code>boolean</code></td>
<td style="height: 20px; width: 332.222px;"><code>Point[] board, Point point</code></td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 200px;"><code>start</code></td>
<td style="height: 20px; width: 78.8889px;"><code>void</code></td>
<td style="height: 20px; width: 332.222px;"><code>Game game</code></td>
</tr>
<tr style="height: 20px;">
<td style="height: 20px; width: 200px;"><code>main</code></td>
<td style="height: 20px; width: 78.8889px;"><code>void</code></td>
<td style="height: 20px; width: 332.222px;">None</td>
</tr>
</tbody>
</table>
<br />
<p></p>
<ul>
<li><code>isFull</code>
<ul>
<li>Check whether any valid moves can be played. Returns true if the board is full (All 64 positions are occupied), false if it is not.&nbsp;</li>
</ul>
</li>
<li><code>contains</code>
<ul>
<li>This method should check if a given point/position in the board is within the given array of points. This is used to check if the user&rsquo;s input is among their valid set of positions (moves) or not.</li>
</ul>
</li>
<li><code>start</code>
<ul>
<li>This method runs the game.
<ul>
<li>The player using black pieces will always start the game.</li>
<li>This method has to handle reading input from the user in order to make a move.
<ul>
<li>In this case, it will take a two digit integer (where the first digit is the row, and the second is the column) from the user to represent a position that they want to move to.</li>
<li>Then, it needs to check whether this position is within this player&rsquo;s valid moves or not. If it is not, you need to keep asking the user until you get a valid position - Use the contains() method.</li>
<li>If the user inputs &lsquo;exit&rsquo;, the game terminates.</li>
</ul>
</li>
<li>Moreover, this method needs to handle cases where one of the players might have no valid moves, and has to skip his turn.</li>
<li>Finally, this method should report the winner at the end of the game.</li>
<li>The game terminates either when both players have no valid moves or when the board is full and there are no empty positions. Hint: the isFull() method may be useful. It also terminates if the players inputs &lsquo;exit&rsquo;.</li>
</ul>
</li>
</ul>
</li>
<li><code>main</code>
<ul>
<li>Creates a Game object and calls the start()&nbsp;method.&nbsp;</li>
</ul>
</li>
</ul>
<p>Additional comments can be found in the Starter Code.&nbsp;</p>
<p></p>
<h3></h3>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="3">Testing</h2>
<h3>Sample Game</h3>
<p>You can use the following sample game to test your implementation.</p>
<pre>  1 2 3 4 5 6 7 8<br />1 _ _ _ _ _ _ _ _<br />2 _ _ _ _ _ _ _ _<br />3 _ _ _ * _ _ _ _<br />4 _ _ * W B _ _ _<br />5 _ _ _ B W * _ _<br />6 _ _ _ _ * _ _ _<br />7 _ _ _ _ _ _ _ _<br />8 _ _ _ _ _ _ _ _<br /><br />Place move (Black): row then column:<br />[56]<br />Black: 4 White: 1<br /><br />  1 2 3 4 5 6 7 8<br />1 _ _ _ _ _ _ _ _<br />2 _ _ _ _ _ _ _ _<br />3 _ _ _ _ _ _ _ _<br />4 _ _ _ W B * _ _<br />5 _ _ _ B B B _ _<br />6 _ _ _ * _ * _ _<br />7 _ _ _ _ _ _ _ _<br />8 _ _ _ _ _ _ _ _<br /><br />Place move (White): row then column:<br />[64]<br />White: 3 Black: 3<br /><br />  1 2 3 4 5 6 7 8<br />1 _ _ _ _ _ _ _ _<br />2 _ _ _ _ _ _ _ _<br />3 _ _ * _ _ _ _ _<br />4 _ _ * W B _ _ _<br />5 _ _ * W B B _ _<br />6 _ _ * W _ _ _ _<br />7 _ _ * _ _ _ _ _<br />8 _ _ _ _ _ _ _ _<br /><br />Place move (Black): row then column:<br />[53]<br />Black: 5 White: 2

&nbsp; 1 2 3 4 5 6 7 8<br />1 \_ \_ \_ \_ \_ \_ \_ \_<br />2 \_ \_ \_ \_ \_ \_ \_ \_<br />3 \_ \_ \_ \_ \_ \_ \_ \_<br />4 \_ \* \_ W B \* \_ \_<br />5 \_ \_ B B B B \_ \_<br />6 \_ \* \_ W \_ \* \_ \_<br />7 \_ \_ \_ \_ \_ \_ \_ \_<br />8 \_ \_ \_ \_ \_ \_ \_ \_

Place move (White): row then column:<br />[66]<br />White: 4 Black: 4</pre><pre>

&nbsp; 1 2 3 4 5 6 7 8<br />1 \_ \_ \_ \_ \_ \_ \_ \_<br />2 \_ \_ \_ \_ \_ \_ \_ \_<br />3 \_ \_ \_ \* \* \_ \_ \_<br />4 \_ \_ \* W B \_ \_ \_<br />5 \_ \_ B B W B \_ \_<br />6 \_ \_ \_ W \* W \_ \_<br />7 \_ \_ \_ \* \* \* \_ \_<br />8 \_ \_ \_ \_ \_ \_ \_ \_<br /><br />Place move (Black): row then column:<br />[75]<br />Black: 6 White: 3

&nbsp; 1 2 3 4 5 6 7 8<br />1 \_ \_ \_ \_ \_ \_ \_ \_<br />2 \_ \_ \_ \_ \_ \_ \_ \_<br />3 \_ \_ \_ \_ \* \_ \_ \_<br />4 \_ \_ \_ W B \* \_ \_<br />5 \_ \* B B W B \* \_<br />6 \_ \* \_ B \_ W \_ \_<br />7 \_ \_ \* \* B \_ \_ \_<br />8 \_ \_ \_ \* \_ \_ \_ \_<br /><br />Place move (White): row then column:<br />[46]<br />White: 6 Black: 4

&nbsp; 1 2 3 4 5 6 7 8<br />1 \_ \_ \_ \_ \_ \_ \_ \_<br />2 \_ \_ \_ \_ \_ \_ \_ \_<br />3 \_ \_ \_ \* \* \* \* \_<br />4 \_ \_ \_ W W W \_ \_<br />5 \_ \_ B B W W \* \_<br />6 \_ \_ \_ B \_ W \_ \_<br />7 \_ \_ \_ \_ B \_ \_ \_<br />8 \_ \_ \_ \_ \_ \_ \_ \_

Place move (Black): row then column:<br />[57]<br />Black: 8 White: 3

&nbsp; 1 2 3 4 5 6 7 8<br />1 \_ \_ \_ \_ \_ \_ \_ \_<br />2 \_ \_ \_ \_ \_ \_ \_ \_<br />3 \_ \_ \_ \_ \_ \_ \_ \_<br />4 \_ \_ \_ W W W \_ \_<br />5 \_ \_ B B B B B \_<br />6 \_ \* \* B \* B \* \*<br />7 \_ \_ \* \* B \* \* \_<br />8 \_ \_ \_ \_ \_ \_ \_ \_

Place move (White): row then column:<br />[65]<br />White: 5 Black: 7<br /><br />&nbsp; 1 2 3 4 5 6 7 8<br />1 \_ \_ \_ \_ \_ \_ \_ \_<br />2 \_ \_ \_ \_ \_ \_ \_ \_<br />3 \_ \_ \* \* \* \* \* \_<br />4 \_ \_ \_ W W W \_ \_<br />5 \_ \_ B B W B B \_<br />6 \_ \_ \_ B W B \_ \_<br />7 \_ \_ \_ \* B \* \_ \_<br />8 \_ \_ \_ \_ \_ \_ \_ \_

Place move (Black): row then column:<br />[35]<br />Black: 13 White: 0

&nbsp; 1 2 3 4 5 6 7 8<br />1 \_ \_ \_ \_ \_ \_ \_ \_<br />2 \_ \_ \_ \_ \_ \_ \_ \_<br />3 \_ \_ \_ \_ B \_ \_ \_<br />4 \_ \_ \_ B B B \_ \_<br />5 \_ \_ B B B B B \_<br />6 \_ \_ \_ B B B \_ \_<br />7 \_ \_ \_ \_ B \_ \_ \_<br />8 \_ \_ \_ \_ \_ \_ \_ \_<br /><br />Black wins: 13:0</pre>
<p>Note: Brackets [] indicate input.&nbsp;</p>
<p></p>
<h3>RunLocalTest</h3>
<p>We have included a program that will allow you to create and run output tests automatically in the Starter Code. This will make it easier for you to verify that each possible progression through your solution is correct. Take a look at <code>RunLocalTest.java</code>. There are many utility features and tools that you do not need to worry about at the moment, instead, focus on the test case. It is included in the Starter Code. Read through it.</p>
<p></p>
<p>You can modify the test to test any method you like by following the same format. You can either download the program and run the main method or use the "Run" button on Vocareum to run the test. You can repeat this process for each path.&nbsp;</p>
<h3>Public Test Cases Note</h3>
<p>For many homeworks and projects, we will give you test cases that correspond to several of the ways we will be testing your program. But, we will not give you test cases for ALL of the ways we will be testing your program. You should think of other test cases to use that will fully test every aspect of every feature of your program. Just because your program passes all the test cases we give you does not mean that it is fully correct and will receive a score of 100.</p>
<hr style="width: 100%; height: auto; color: #ffffff; border: 1px inset #cccccc;" />
<h2 id="4">Submit</h2>
<p>After testing your solution and verifying that it meets the requirements described in this document, you can submit on Vocareum.&nbsp; You have 10 submission attempts to achieve full points.&nbsp;</p>
<p></p>
</div>
</div>
<footer></footer></main></div>
</body>

</html>
