---
title: "Problem 2"
heroStyle: background
weight: 3
showRelatedContent: false
---

<strong>The second problem we are going to look at is from the chapter 3 homework</strong>

<h2>Bean counting</h2>
<blockquote>You can get the Nth character, or letter, from a string by writing [N] after the string (for example, string[2]). The resulting value will be a string containing only one character (for example, "b"). The first character has position 0, which causes the last one to be found at position string.length - 1. In other words, a two-character string has length 2, and its characters have positions 0 and 1.

Write a function called countBs that takes a string as its only argument and returns a number that indicates how many uppercase B characters there are in the string.

Next, write a function called countChar that behaves like countBs, except it takes a second argument that indicates the character that is to be counted (rather than counting only uppercase B characters). Rewrite countBs to make use of this new function.

// Your code here.

console.log(countBs("BOB"));</br>
// → 2</br>
console.log(countChar("kakkerlak", "k"));</br>
// → 4
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
function countBs(str) {   
  return countChar(str);
}
function countChar(str, charToCount = 'B') { 
  let count = 0;
  for (let i = 0; i < str.length; i++) {
    if (str[i] === charToCount) {
      count++;
    }
  }
  return count;
}
console.log(countBs("BOB"))

console.log(countChar("kakkerlak", "k"))
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
<code>
function countBs(str) {   </br>
  return countChar(str);</br>
}</br>
function countChar(str, charToCount = 'B') { </br>
  let count = 0;</br>
  for (let i = 0; i < str.length; i++) {</br>
    if (str[i] === charToCount) {</br>
      count++;</br>
    }
  }
  return count;</br>
}
console.log(countBs("BOB"))</br>
// → 2</br>
console.log(countChar("kakkerlak", "k"))</br>
// → 4 
</code>
<h3>Explanation</h3>
<code>function countBs(str) {</code>
<blockquote>
this function meets the homework requirment as this just does the counting of the B's and it thats that string that it is given.
</blockquote>
<code>return countChar(str);}</code>
<blockquote>
this allows for you to change the character in which you want counted in this case we can now do the letter K.
</blockquote>
<code>function countChar(str, charToCount = 'B') {</code>
<blockquote>
this starts the function and makes countchar work it is given the str that it needs to take for example BOB and it is told which character to count in this case the B.
</blockquote>
<code> let count = 0;</code>
<blockquote>
it starts off by making the count and that value has to start at 0.
</blockquote>
<code> for (let i = 0; i < str.length; i++) {</code>
<blockquote>
this then starts a for loop that that makes i equal to 0 it then checks to see if i is less then the lenght of the string we are given so if the word is "BOB" it would run this code if it was "" meaning blank it would have nothing to count it then adds one to i to make sure we go though every charater in the string.
</blockquote>
<code> if (str[i] === charToCount) {</code>
<blockquote>
this then does an if statement that says if the character in the string is equal to the character that we are tring to count then go onto the next code. so for example is we have the string "BOB" and we are counting B's then at str[0] we would have a B but since the charToCount is equal to B then we would contuine.
</blockquote>
<code>  count++;}</code>
<blockquote>
after the previous code is run and the if statement turns out to be turn then it will run this code which just takes the count and adds one to it.
</blockquote>
<code>return count;}</code>
<blockquote>
ones the entire string is done and theres nothing left to count it will run this line which returns the count of whatever value we need.
</blockquote>
<code>console.log(countBs("BOB"))</br>
console.log(countChar("kakkerlak", "k"))</code>
<blockquote>
this then just makes it so we can see the code that we want and it also defines what string we want to be counted.
</blockquote>

<h3>Sources</h3>
Click <a href="https://eloquentjavascript.net/03_functions.html" target="_blank">Here</a> for the link to the textbook for this problem.
</br>
Click <a href="https://github.com/nunocoracao/blowfish" target="_blank">Here</a> for the link to the theme for blowfish on github.