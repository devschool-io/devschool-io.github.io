---
layout: post
title:  "Jquery Methods"
date:   2015-04-22 17:29:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127851197" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>

<div class="not-on-video">
  <h2>Jquery Methods</h2>
  <p>Here we are introducing some simple methods in Jquery.</p>

  <ul>
    <li>show() and hide()</li>
    <li>toggle()</li>
  </ul>
</div>  



index.html

{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="css/example.css">
  </head>
  <body>
    <h1>Checkout this volcano</h1>
    <div class="normal-volcano">
      <h4>What a nice looking volcano...</h4> 
      <img src="images/volcano.jpg">
    </div>  
    <div class="erupting-volcano">
      <h4>Everyone run for your lives!</h4> 
      <img src="images/erupting.jpg">
    </div>
    <script src="scripts/jquery-1.11.3.js"></script>
    <script src="scripts/myscript.js"></script>
  </body>  
</html> 

{% endhighlight %}

example.css

{% highlight css %}

img {
  width: 400px;
  height: 400px;
}

.erupting-volcano {
  display: none;
}

{% endhighlight %}

myscript.js

{% highlight JavaScript %}

$("img").on("click", function(){
  $(".erupting-volcano").toggle();
  $(".normal-volcano").toggle();
})

{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Create a webpage with 2 images, use divs to separate the images.  Hide one of the images using CSS rules.</li>
  <li>Add a listener event for "img" on "click", use the methods show() and hide() on interact with the images.</li>
  <li>Now use toggle() instead of show() and hide().</li>
  <li>Now try the methods fadeIn() and fadeOut() instead of toggle.</li>
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
