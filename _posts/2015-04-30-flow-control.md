---
layout: post
title:  "Control Flow"
date:   2015-05-01 21:58:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127754068" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>


<br><br>

<div class="not-on-video">
  <h2>Control Flow with If and Else Statements.</h2>
  <p>We will use control flow to capture some input from the user.  Depending on the input we will display specific content.</p>
</div> 

index.html

{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="css/bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="css/example.css">
    <script src="scripts/jquery-1.11.3.js"></script>
    <script src="scripts/myscript.js"></script>
  </head>
  <body>
    <h1>Welcome to "Once In a Lifetime" theme park:</h1>
    <h4>We make safety our least priority.</h4>
    <div class="tall-enough">
      <h5>List of rides you can go on:</h5>
      <ul>
        <li>The Roller Coaster of Doom (waiver required).</li>
        <li>No tears left Haunted House.</li>
        <li>Out of Control Carousel</li>
      </ul>
    </div>
    <div class="exact-height">
      <h5>Let me bring my meter; We have to make sure. Are you wearing shoes to make you taller?</h5> 
    </div>  
    <div class="not-tall-enough">
      <h5>You are not tall enough for our rides. Please go wait by the water fountain.</h5> 
    </div>
  </body>  
</html>

{% endhighlight %}


myscript.js

{% highlight JavaScript %}

$(document).ready(function(){
  var tallEnough = parseInt(prompt("What is your height in cmts. e.g 173 cmts"));

  // I will use parseInt() to make sure that we convert the user input to an integer.  Remember parseInt("90") returns 90
  // This was NOT in the video

  if(tallEnough > 100){
    $(".tall-enough").fadeIn();
  } else if(tallEnough === 100){
    $(".exact-height").fadeIn();
  } else {
    $(".not-tall-enough").fadeIn();
  }
})

{% endhighlight %}


CSS
{% highlight css %}

.tall-enough {
  display: none;
}

.not-tall-enough {
  display: none;
}

.exact-height {
  display: none;
}

{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Asks users a question to create your own control flow website.  Be creative.</li>
  <li>If your logic is not working, make sure to use the parseInt() function to change a string to an integer.</li>
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
