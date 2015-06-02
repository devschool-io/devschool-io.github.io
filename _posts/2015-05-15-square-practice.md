---
layout: post
title:  "Square or Rectangle (Practice Prob.)"
date:   2015-05-15 21:58:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/128289625" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>



<br><br>

<div class="not-on-video">
  <h2>Practice Problem</h2>
  <p>Please finish this problem before class starts.</p>

  <p>Notice how we are separating our logic( squareOrRectangle function) from the user interface ( $("form").on ... ) section of the code.  This is very helpful to organize our code.</p>
</div> 

index.html

{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <title>Square or Rectangle</title>
    <link rel="stylesheet" type="text/css" href="css/bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="css/styles.css">
    <script src="scripts/jquery-1.11.3.js"></script>
    <script src="scripts/myscript.js"></script>
  </head>
  <body>
    <div class="container">
      <h1>Square or Rectangle</h1>
      <form>
        <div class="form-group">
          <label>Side A</label>
          <input type="text" id="side-a" placeholder="Side A">
        </div> 
        <div class="form-group">
          <label>Side B</label>
          <input type="text" id="side-b" placeholder="Side B">
        </div>  
        <button type="submit" class="btn btn-success">Submit</button>
      </form>
      <h2><span id="result"></span></h2>  
    </div>  
  </body>
</html>

{% endhighlight %}


myscript.js

{% highlight JavaScript %}

$(document).ready(function(){

  function squareOrRectangle(sideA, sideB){
    if (sideA > 0 && sideB > 0){
      if(sideA === sideB){
        return "square";
      } else {
        return "rectangle";
      }
    } else {
      return "invalid input";
    }
  }

  $("form").on("submit", function(event){
    event.preventDefault();

    var sideA = parseInt($("input#side-a").val());
    var sideB = parseInt($("input#side-b").val());

    var result = squareOrRectangle(sideA, sideB);

    $("span#result").text(sideA + " X " + sideB + " is a " + result);
  })
})

{% endhighlight %}


<p>Try the following:</p>
<ul>
  <li>Watch the video and rewrite the solution to this problem.  Try not to copy the code verbatim. Analyze what every piece of code is doing.</li>
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
