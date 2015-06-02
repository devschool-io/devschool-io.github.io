---
layout: post
title:  "Jquery - Using Document Ready"
date:   2015-04-29 19:29:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127521191" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>

<h2>Using $(document).ready()</h2>

<p>$(document).ready() allows us to wait until all the web elements are loaded before any JavaScript code is loaded. More info <a href="http://learn.jquery.com/using-jquery-core/document-ready/" target="_blank">here</a></p>

<p>Watch the video and check out our implementation of $(document).ready()</p>

index.html

{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="css/example.css">
    <script src="scripts/jquery-1.11.3.js"></script>
    <script src="scripts/myscript.js"></script>
  </head>
  <body>
    <div class="actions">
      <button id="bark">Bark</button>
      <button id="growl">Growl</button>
      <button id="hide">Hide</button>
      <button id="blue">Background Blue</button>
      <button id="none">Remove Background</button>
    </div>
    <div class="activity-tracker">
      <ul></ul>
    </div>  
  </body>  
</html>


{% endhighlight %}

example.css

{% highlight css %}

.turn-blue {
  background-color: blue;
}

{% endhighlight %}

myscript.js

{% highlight javascript %}

$(document).ready(function(){
  $("button#blue").on("click", function(){
    var makeBlue = "Full moon tonight!";
    $(".activity-tracker ul").prepend("<li>"+ makeBlue +"</li>")
    $("body").addClass("turn-blue");
  })

  $("#none").on("click", function(){
    var makeClear = "It is daytime";
    $(".activity-tracker ul").empty().prepend("<li>" + makeClear +"</li>")
    $("body").removeClass("turn-blue");
  })

  $("button#bark").on("click", function(){
    $(".activity-tracker ul").prepend("<li>Woof woof!</li>")
  })

  $("button#growl").on("click", function(){
    $(".activity-tracker ul").prepend("<li>Was that a bear?</li>")
  })

  $("button#hide").on("click", function(){
    $(".activity-tracker ul").prepend("<li>Climb up a tree!</li>")
  })
})

{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Load the scripts inside the head tag and use $(document).redy() to make it work (use any of examples you worked on previously).</li>
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
