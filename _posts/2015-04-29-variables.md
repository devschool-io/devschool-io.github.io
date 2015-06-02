---
layout: post
title:  "Variables"
date:   2015-04-29 17:29:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127851207" width="1200" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>

<div class="not-on-video">
  <h2>Variables</h2>
  <p>Variables are used when you want to store a value for later use.</p>
  <p>We are going to be using variables on the code we wrote in the previous lesson.</p>
</div>  

<div class="not-on-video">
  <h2>Local Variables</h2>
  <p>Local variables are only available in the nested code of block where they are defined.  Once we move out of the block of code (often called "scope", the variable will no longer be available.  Watch the video for further explanation.</p>
  <p>Local variables are always defined with the "var" keyword.  For example, var exampleGreeting = "hello" is a local variable.  exampleGreeting is only available within the scope where it was defined.</p>
</div> 

<div class="not-on-video">
  <h2>Global Variables</h2>
  <p>Global variables are available at all levels of the codes, once the global variable is defined you can access it basically anywhere.</p>
  <p>We define global variables without using the keyword "var". So, globalGreeting = "hello"  would be a global variable.</p>
  <p>Using global variable is a bit dangerous as you can loose track of names and start to overwrite global variables causing your code to have bugs.  For now, we are going to avoid using global variables.</p>
</div>   

index.html

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

example.css

{% highlight css %}

.turn-blue {
  background-color: blue;
}

{% endhighlight %}

myscript.js

{% highlight javascript %}

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


{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Try to use local variables for the strings inserted in the li's.</li>
  <li>Recreate the undefined error for a local variable and try to understand why it happened.</li>
  <li>Understand the differences between a global and local variable.</li>
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
