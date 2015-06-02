---
layout: post
title:  "Jquery Manipulation"
date:   2015-04-23 20:29:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127943484" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>

<div class="not-on-video">
  <h2>Manipulation in Jquery</h2>
  <p>We will now learn how to manipulate web elements.  We will start by adding and removing classes to elements.  Then we will try to add list item (li) to empty unordered list (ul).</p>
</div>  

<figcaption>index.html</figcaption>

{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="css/example.css">
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
    <script src="scripts/jquery-1.11.3.js"></script>
    <script src="scripts/myscript.js"></script>
  </body>  
</html>

{% endhighlight %}

<figcaption>myscript.js</figcaption>
{% highlight javascript %}

$("button#blue").on("click", function(){
  $(".activity-tracker ul").prepend("<li>Full moon tonight!</li>")
  $("body").addClass("turn-blue");
})

$("#none").on("click", function(){
  $(".activity-tracker ul").empty().prepend("<li>It is daytime!</li>")
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

{% endhighlight %}

<figcaption>example.css</figcaption>
{% highlight css %}

.turn-blue {
  background-color: blue;
}

{% endhighlight %}



<p>Try the following:</p>
<ul>
  <li>Create a simple web page that changes the background from red, blue and yellow.  Also, add a button remove the background.</li>
  <li>Add a button to the web page "Ring bell" and that adds "Ding dong" to the screen (use and ul and an li to do this. Also, the append or prepend method).</li>
  <li>Add more actions with buttons to the page, be creative.</li>
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
