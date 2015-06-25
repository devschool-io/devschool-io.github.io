---
layout: post
title:  "JavaScript Fast Intro"
date:   2015-03-31 16:29:48
categories: JavaScript
tags: [javascript]
---
This is a quick intro to JavaScript. The most used programming language on the web.
Your web browser (Google Chrome, Firefox, Internet Explorer or Safari) right now is running JavaScript code in the background.

<p>If you don't have Google Chrome please download it <a href="https://www.google.com/chrome/browser/desktop/" target="_blank">Here.</a></p>

<p>In some of the example below I use <a href="https://jsfiddle.net/" target="_blank">JSFiddle.net</a> for quicker demonstrations purposes.</p>

<iframe width="640" height="480"  src="http://www.youtube.com/embed/3jVmo73VBFo?VQ=HD480" frameborder="0" allowfullscreen></iframe>
<br><br>
<div class="not-on-video">
  <h2>Chrome Console:</h2>
  <p>Open the console in Chrome with following command:</p>
  <p>Windows/Linux: Control + Shift + j</p>
  <p>Mac: Command + Alt + j</p>
</div>  

<h3>Comments</h3>

{% highlight JavaScript %}

// This is a one line comment in JavaScript. This line of code will not run.
// You create comments by adding "//" before every line.
// Comments are important to document code or explain things.

/*
This
is
a multiline comment.  Instead of writing "//" before every line
*/

{% endhighlight %}

<h3>Arithmetic</h3>

{% highlight JavaScript %}

// try typing these directly on your console, right after ">" and press enter.

// addition

1 + 1

// Press enter. The result should be:

> 2

// Multiplication

2 * 2

> 4

// Division

10 / 5

> 2

// Modulus or % gives the remainder of a division

10 % 2

> 0

// remainder is 0

11 % 2

> 1

// remainder is 1

{% endhighlight %}

<h3>Strings</h3>

{% highlight JavaScript %}

// Strings: A string can be any text inside double or single quotes

"Hello"

// "hello" is a string, you can also add strings together.

"Hello" + "Everyone"

> "HelloEveryone"

// "1" is also a string. The number 1 is not the same as the string "1".
// Try adding "1" + "1" together.

"1" + "1"

// this is equal to "11"

{% endhighlight %}

<h3>Booleans</h3>

{% highlight JavaScript %}

// Booleans are either true or false

1 + 1 === 2

// true

1 + 1 === 3

// false

"1" === 1

// false

1 < 2

// true

2 < 2

// false

2 <= 2

// true, <= this is less than or equal to.  The inverse is >= greater than or equal.

11 % 2 === 1

// true

10 % 2 === 0

// true

// Exercise hint 1: Maybe something like this could be useful.

{% endhighlight %}


<h3>Variables</h3>

{% highlight JavaScript %}
// Variables
// We can save a value in a variable for later use.
// Let's create the variable foo and assign the value 99 to it.

var foo = 99;

// let's call foo in the console.

foo

// You have called your variable foo and its value is 99
// Now, you can manipulate the value in foo if you like.

foo = foo + 1;

// call foo again and see what the value is now.

{% endhighlight %}


<h3>Conditional Statements</h3>
<h4>Conditional statements are used to perform different actions
based on different conditions.</h4>
<h4>An <strong>if Statement</strong> is a type of conditional statement.</h4>
{% highlight JavaScript %}

if(1 + 1 === 2){
  console.log("Hello");
}

// Since 1 + 1 === 2 is true, you should see "Hello" on the console.


if(10 / 5 === 3){
  console.log("Hello");
}

// Since 10 / 5 === 3 is false, you should NOT see "Hello" on the console.


{% endhighlight %}

<h4>An <strong>else Statement</strong> is also type of conditional statement.</h4>

{% highlight JavaScript %}

// You can also add an else statement after the if statement
// else statements only run if the if statement is false.

if(10 / 5 === 3){
  console.log("Hello");
} else {
  console.log("10 divided by 5 does not equal 3, this is why you are seeing this message in your log.")
}

{% endhighlight %}

<h3>For Loops</h3>

<p>Imagine having to write something a hundred times. For example, logging the numbers from 1 to 100.  Manually, you would write something like this:</p>

{% highlight javascript %}
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
...
console.log(100);
{% endhighlight %}

<p>These are 100 lines of code, way too long.  We could use a for loop to cut down on all the work.</p>

{% highlight javascript %}

/*
for loops take in 3 arguments
first: var i = 1 is the starting point of the loop
Second: i <= 100 sets the limit
Third: i = i + 1 adds 1 to i everytime the loop starts
*/

for(var i = 1; i <= 100; i = i + 1){
  console.log(i);
}

/*
We need to increment i by one to make the loop work.
If you leave i at the initial value of 1 the second argument
i <= 100 will always be true (since i is 1, 1 will always be less than equal 100).
If i <= 100 is always true, the loop would go on forever and crash your computer.
So this is why we need to have a counter that increments in the loop (i = i + 1).
Once i is equal to 101, by adding one to i a hundred times.  The second argument would be false and
loop would terminate.  This is why we need the third argument i = i + 1
You can also write i = i + 1 like this i++
*/

// We can also have if statements inside a for loop

for(var i = 1; i <= 100; i = i + 1){
  if ( i + 5 === 10){
    console.log("Is the variable i currently 5?");
    // let's check and see, remember this line is a comment
    console.log(i);
    // check your log and see what i was.
  }
}

// Run the for loop above and see what it logs in the console.
// Remember to keep the right notation.  A missing parenthesis or curly bracket "{"
// will break your code and throw an error.

// this loop ran 100 times but only ran the if block of code when i was 5 and
// it skipped the if block of code for all the other numbers.


// Through in an else statement inside the for loop too.

for(var i = 1; i <= 5; i = i + 1){
  if ( i + 5 === 10){
    console.log("Who ate my taco?");
  } else {
    console.log(i);
  }
}

// Exercise hint 2: use a for loop with if and else statements to log the exercise problem.
// running the above loop logs the following:

> 1
> 2
> 3
> 4
> "Who ate my taco?"

// this loop ran 5 times but only when i = 5 the if statement is true and
// it logged: "Who ate my taco?",  else ran for all the other numbers logging only the variable i.

{% endhighlight %}

<h2>Exercise:</h2>
<p>&nbsp;Write some code that loops through the numbers from 1 to 100, if the number is divisible by 3 print <em>"Fizz"</em>. If the number is divisible by 5 print <em>"Buzz"</em>. If the number is divisible by 5 AND 3 print <em>"FizzBuzz"</em>, else just print the number.</p>
<p>Sample output:</p>
<ul class="code">
  <li style="list-style-type: none">> 1</li>
  <li style="list-style-type: none">> 2</li>
  <li style="list-style-type: none">> "Fizz"</li>
  <li style="list-style-type: none">> 4</li>
  <li style="list-style-type: none">> "Buzz"</li>
  <li style="list-style-type: none">> "Fizz"</li>
  <li style="list-style-type: none">> 7</li>
  <li style="list-style-type: none">> 8</li>
  <li style="list-style-type: none">> "Fizz"</li>
  <li style="list-style-type: none">> "Buzz"</li>
  <li style="list-style-type: none">> 11</li>
  <li style="list-style-type: none">> "Fizz"</li>
  <li style="list-style-type: none">> 13</li>
  <li style="list-style-type: none">> 14</li>
  <li style="list-style-type: none">> "FizzBuzz"</li>
  <li style="list-style-type: none">> 16</li>
  <li style="list-style-type: none">> ...</li>
</ul>

<p>Then go to <a href="https://jsfiddle.net/" target="_blank">JSFiddle.net</a> and create a new fiddle with your code.  Run it and test if the output is correct.</p>
<p style="color:red">If you are getting errors, you might be missing some "}", "(" or ";" on your code.</p>

<div id="disqus_thread"></div>
<script type="text/javascript">
    /* * * CONFIGURATION VARIABLES * * */
    var disqus_shortname = 'devschool';

    /* * * DON'T EDIT BELOW THIS LINE * * */
    (function() {
        var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
        dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
        (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>
