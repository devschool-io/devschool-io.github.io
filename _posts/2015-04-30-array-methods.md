---
layout: post
title:  "Array Methods"
date:   2015-04-30 21:58:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/128020272" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>


<br><br>

<div class="not-on-video">
  <h2>Array Methods</h2>
  <ul>
    <li>pop() : removes the last element of the array and returns it. </li>
    <li>push() : adds an element at the end and returns the arrays length.</li>
    <li>shift() : removes the first element in the array and returns it.</li>
    <li>unshift() : adds an element at the beginning and returns the arrays length </li>
    <li>join() : joins every element of the array as a single string.</li>
    <li>indexOf() : if it finds an element it returns it's index else it returns -1. </li>
  </ul>

  <p>Check the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype#Methods" target="_blank">Mozilla page</a> for more info</p>
</div> 

<h2></h2>



{% highlight JavaScript %}

var example = ["hello", "there"];

// call example

example

// returns ["hello", "there"]

example.pop()

// pop() removes the last element of the array and returns it.
// returns "there"

example

// returns ["hello"]

// Let's add "there" back into the array

example.push("there")


// push() adds an element at the end and returns the arrays length.
// should return 2 (length of the array; how many elements in the array)

example

// returns ["hello", "there"]

example.shift()

// Shift removes the first element in the array and returns it.
// returns "hello"

example

// returns ["there"]

// Let's add "hello" back into the array

example.unshift("hello")

// unshift adds an element at the beginning and returns the arrays length.
// returns 2, the length of the array

example

// returns ["hello", "there"]

// join method, joins every element in the array.

example.join()

// each element inside the string will be separated by a comma by default.

// returns "hello,there"

example.join(", ");

// If we add an argument to the join() method we can change how it separates each element.
// every element will be separated by " " (space)
// returns "hello there"

example.join(", ");

// returns "hello, there"


example.indexOf("hello")

// indexOf returns the index if it matches an element.
// otherwise it returns -1
// returns 0, as "hello" is the first element of the array

example.indexOf("bye")

// returns -1, "bye" is not present in the array.

example.indexOf("there")

// returns 1

{% endhighlight %}


<p>Try the following:</p>
<ul>
  <li>Build your own array.  You can use strings, numbers, booleans (true or false) and even variables.</li>
  <li>Use pop(), push(), shift() and unshift() on your array.</li>
  <li>Use join() to turn your array into a string.</li>
  <li>Use indexOf() to find an element of an array.</li>
</ul> 


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
