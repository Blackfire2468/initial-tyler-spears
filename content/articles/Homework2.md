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

</blockquote>
<code>return countChar(str);}</code>
<blockquote>

</blockquote>
<code>function countChar(str, charToCount = 'B') {</code>
<blockquote>

</blockquote>
<code> let count = 0;</code>
<blockquote>

</blockquote>
<code> for (let i = 0; i < str.length; i++) {</code>
<blockquote>

</blockquote>
<code> if (str[i] === charToCount) {</code>
<blockquote>

</blockquote>
<code>  count++;}</code>
<blockquote>

</blockquote>
<code>return count;}</code>
<blockquote>

</blockquote>
<code>console.log(countBs("BOB"))</br>
console.log(countChar("kakkerlak", "k"))</code>
<blockquote>

</blockquote>