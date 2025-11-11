---
title: "Problem 1"
heroStyle: background
weight: 2
showRelatedContent: false
showAuthor: true
showAuthorBottom: false
---
<strong>The first problem we are going to look at is one from the chaper two homework.</strong>

<h2>ChessBoard</h2>
<blockquote> Write a program that creates a string that represents an 8×8 grid, using newline characters to separate lines. At each position of the grid there is either a space or a "#" character. The characters should form a chessboard. 

<p>Passing this string to console.log should show something like this:

<p> # # # # </br>
# # # # </br>
 # # # #</br>
# # # # </br>
 # # # #</br>
# # # # </br>
 # # # #</br>
# # # #
</p>
When you have a program that generates this pattern, define a binding size = 8 and change the program so that it works for any size, outputting a grid of the given width and height.
</p>
</blockquote>
<h3>My Answer</h3>
<p> Explanation of how the code works below</p>
<code>let size = 8;</br>
let board = "";
</br>
for (let y = 0; y < size; y++) {</br>
  for (let x = 0; x < size; x++) {</br>
    if ((x + y) % 2 == 0) {</br>
      board += " ";</br>
    } else {</br>
      board += "#";}</br>
  }</br>
  board += "\n";}
</br>
console.log(board)
</code>

<h3>Explanation</h3>
<p>In order to explain the code we will take it line by line first lets start with</br>
<code>let size = 8;  
<blockquote>
this determines the size of the board so in this case it would be an 8x8 board if we changed the number to 9 it would become a 9x9 board and so on as that number changes.
</blockquote>
let board = "";</code>
<blockquote>
This makes the board as a string that can be printed out. This allows the board start with empty characters
</blockquote>
<code>for (let y = 0; y < size; y++) {</code>
<blockquote>

</blockquote>
<code>for (let x = 0; x < size; x++) {</code>
<blockquote>

</blockquote>
<code>if ((x + y) % 2 == 0) {</code>
<blockquote>

</blockquote>
<code>board += " ";</code>
<blockquote>

</blockquote>
<code>} else {</br>
      board += "#";}</code>
<blockquote>

</blockquote>
<code>}</br>
  board += "\n";}</code>
<blockquote>

</blockquote>
<code>console.log(board)</code>
<blockquote>

</blockquote>