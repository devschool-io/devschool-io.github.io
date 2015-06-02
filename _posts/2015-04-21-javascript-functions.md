---
layout: post
title:  "JavaScript Functions"
date:   2015-04-21 16:29:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127501893" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>

<div class="not-on-video">
  <h2>Functions in JavaScript</h2>
  <p>A function is something that does something.  They are very similar to methods but they can be called on their own.  While methods (previous lesson) always belong to something.</p>
</div>  


{% highlight JavaScript %}
// for example parseInt() is a function, it tries to change a string in a number if it can. 
// Calling parseInt("1"), should return 1 without the quotes, an actual number.

parseInt("4");

> 4

// Remember when we called toFixed() on a number, that method belongs to the number.
// example, 4.25.toFixed();
// You cannot call toFixed() on it's own. So toFixed() is a method.

alert("Good morning Guatemala");

// You should see a window pop-up on your browser.  
// alert() is function that takes in an argument and displays a box with the argument on the browser.

prompt("What is your age?");

// This function will pop a box open that asks user for something and returns the user input.
// In order to use the prompt function correctly let's save the user input in a variable.

var age = prompt("What is your age?");

// calling age would return the user input

confirm("Do you like programming?");

// the confirm function only returns true or false (know as booleans)


// Writing a Function

// When writing multiline code in your Chrome console use shift + enter to make a new line. Once you are ready you can press "enter" to evaluate your code.

var numberSquared = function(number){
  return number * number;
}

// now let's try are function out

numberSquared(4);

> 16

// remember you can also store the functions return value in a variable.  
//

var fourSquared = numberSquared(4);

fourSquared

> 16

// Now try to write a function that divides a number by 2 and returns the calculation.

{% endhighlight %}

<p>Try the following in your Chrome console:</p>
<ul>
  <li>Use parseInt() to change "99" as number.</li>
  <li>Use alert() to display an alert with any message of your choosing.</li>
  <li>Use prompt to as yourself a question.  Then assign to a variable and call it to see if it was assigned correctly.</li>
  <li>Write a function that takes in a number and returns the number multiplied by 2 (e.g  calling the function timesTwo(6) should console.log 12 on your Chrome console.</li>
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
