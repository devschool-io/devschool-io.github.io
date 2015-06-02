---
layout: post
title:  "Jquery Traversing"
date:   2015-04-23 17:29:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127943485" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>
<div class="not-on-video">
  <h2>Traversing in Jquery</h2>
  <p>We will now learn how to navigate the through web elements with Jquery.  We will be able to find a specific element so that we can interact with it.</p>
</div>  

<br>


<p>Open up the console in Chrome, make sure you loaded Jquery (you won't be able to use it if you don't).</p>

index.html

{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="css/example.css">
  </head>
  <body>
    <div class="container">
      <h2>These are types of Nuts:</h2>
      <ul class="nuts">
        <li>Almonds</li>
        <li>Cashews</li>
        <li>Hazelnuts</li>
      </ul> 
      <h2>These are types of Apples:</h2>
      <ul class="apples">
        <li>Fiji</li>
        <li>Granny</li>
      </ul>
    </div>  
    <script src="scripts/jquery-1.11.3.js"></script>
    <script src="scripts/myscript.js"></script>
  </body>  
</html>

{% endhighlight %}

{% highlight javascript %}

// Commands used in the console

$("ul")

$("ul.nuts")

$("ul.apples")

$("ul.apples li")

$("ul.apples li:first")

$("ul.apples").find("li")

$("ul.apples").find("li").first()

$("ul.apples").find("li").last()

$("ul.apples").find("li").last().parent();

$("ul.apples").siblings();

{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Get the siblings of the almond list item.</li>
  <li>Get the parent of the hazelnut list item.</li>
  <li>Try to use the next() or prev() methods on an element.  More info here <a href="https://api.jquery.com/category/traversing/tree-traversal/" target="_blank">Jquery Tree Traversal</a></li>
  <li>Try to chain methods together for example $("ul.apples").find("li").last() is chaining two methods.  See how far you can go..</li>
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
