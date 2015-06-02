---
layout: post
title:  "JavaScript Methods"
date:   2015-04-20 16:29:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127851206" width="1200" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>


<div class="not-on-video">
  <h2>Methods</h2>
  <p>Methods are used when you want to perform an action on something.</p>
  <p>Let's fire up the console in Chrome (mac/linux alt + command + j or windows control + shift + j).</p>
</div>  



{% highlight JavaScript %}

var exampleString = "I burnt my toast today";

// let's call the method slice on string

exampleString.slice(0,1)

// the numbers inside slice "0,1" are telling slice to get the characters from the position 0
// of the string and up to 1 but not including it.
// Otherwise slice would return "I " not just "I".  Notice the spaces are counted.
// These are also known as arguments.  Inputs that give instructions for methods to perform certain actions.


// The slice method will return "I"

exampleString.slice(2,7);

// The slice method will return "burnt"

// try it out, see if you can slice "toast"

// Now let's try the method toFixed() on a number.
// toFixed() returns the numbers as a string keeping the decimals places if an argument is provided.

var exampleNumber = 4.25;

exampleNumber.toFixed()

> "4"

// now let's add an argument to it.  

exampleNumber.toFixed(4)

> "4.2500"


{% endhighlight %}

<p>Try the following in your Chrome console:</p>
<ul>
  <li>Declare a string in a variable name of your choosing. (e.g var tooMuch = "blah")</li>
  <li>Use slice to get any words out of the sentence.  Play around about it with it. </li>
  <li>Declare a number in a variable.  Use the toFixed() method on it.  Remember the toFixed() method is only available if you are using it on a number.</li>
  <li>Use the toString() on your number variable to return it's  value as a string.</li>
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
