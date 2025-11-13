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

Here’s some interactive code you can try to test it out:

<html>
  <style>
    textarea {
      width: 100%;
      height: 150px;
      font-family: monospace;
      font-size: 14px;
      border: 1px solid #000000ff;
      border-radius: 5px;
      padding: 10px;
      background-color: #fff;
        background-color: #1e1e1e; 
    color: #ffffff; 
    }
    button {
      background-color: #0078d7;
      color: white;
      border: none;
      padding: 10px 20px;
      margin-top: 10px;
      border-radius: 4px;
      cursor: pointer;
    }
    #output {
      margin-top: 10px;
      background: #272822;
      color: #f8f8f2;
      padding: 10px;
      border-radius: 5px;
      white-space: pre-wrap;
    }
  </style>

  <textarea id="codeArea">
 let size = 8;
let board = "";
for (let y = 0; y < size; y++) {
  for (let x = 0; x < size; x++) {
    if ((x + y) % 2 == 0) {
      board += " ";
    } else {
      board += "#";}
  }
    if (y < size - 1) board += "\n";
}
console.log(board)
  </textarea>
  <br>
  <button onclick="runCode()">Run Code</button>
  <div id="output"></div>

  <script>

//Chatgpt did help me with the code runner and how to set it up so it actually ran the code i thought it would be a good touch and feel more interactive.

    function runCode() {
      const code = document.getElementById("codeArea").value;
      const outputDiv = document.getElementById("output");
      outputDiv.innerHTML = "";
      const oldLog = console.log;
      console.log = function(msg) {
        outputDiv.innerHTML += msg + "\\n";
      };
      try {
        eval(code);
      } catch (err) {
        outputDiv.innerHTML += "Error: " + err.message;
      }
      console.log = oldLog;
    }
  </script>
</html>

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
 if (y < size - 1) board += "\n";
}
</br>
console.log(board)
</code>

<h3>Explanation</h3>
<p>In order to explain the code we will take it line by line:</br>
<code>let size = 8;  
<blockquote>
this determines the size of the board so in this case it would be an 8x8 board if we changed the number to 9 it would become a 9x9 board and so on as that number changes.
</blockquote>
let board = "";</code>
<blockquote>
This makes the board as a string that can be printed out. This allows the board start with empty characters.
</blockquote>
<code>for (let y = 0; y < size; y++) {</code>
<blockquote>
this for loop then makes y equal 0 which is like a y-axis on a graph so row 1 gets created then it checks to make sure that y is less than the size that we made the board so in this case y has to be less than 8. Then at the end of this for loop it adds 1 to the y to tell it to go down a row.
</blockquote>
<code>for (let x = 0; x < size; x++) {</code>
<blockquote>
this for loop that is in the previous for loop make x equal 0 similar to the other loop with y this does the columns instead of the rows and in order to keep it a square it also has to check to make sure that x is less than the size. after that it adds one to the x and goes until it hits 8 at that point it returns to the previous for loop and does it all again.
</blockquote>
<code>if ((x + y) % 2 == 0) {</code>
<blockquote>
this if statement says that if x and y added together are divisible by 2 meaning that if x is 5 and y is 7 then that would be 12 then it would divide until the remainder is either 1 or 0 in this case if the value is 0 then it would do the statement below otherwise it will go to the else.
</blockquote>
<code>board += " ";</code>
<blockquote>
this is the statement that if x and y added are divisible by 2 then it will make that spot on the board a blank meaning a space or no character.
</blockquote>
<code>} else {</br>
      board += "#";}</code>
<blockquote>
this else statement says is if the previous statement is not true and x plus y can not be divided by 2 then it is going to make a # on the board.
</blockquote>
<code>}</br>
 if (y < size - 1) board += "\n";}
 </code>
<blockquote>
this if statement is outside of the second loop but in the first one and this makes the new lines for the board so when the y and x are done with the row they are on this will make a new line this stops before the end as you do not need a new line after the final row.
</blockquote>
<code>console.log(board)</code>
<blockquote>
this just produces the code somewhere the viewer can see it so you know it actually works.
</blockquote>

<h3>Sources</h3>
Click <a href="https://eloquentjavascript.net/02_program_structure.html" target="_blank">Here</a> for the link to the textbook for this problem.
</br>
Click <a href="https://github.com/nunocoracao/blowfish" target="_blank">Here</a> for the link to the theme for blowfish on github.