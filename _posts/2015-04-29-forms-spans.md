---
layout: post
title:  "Forms with Spans"
date:   2015-04-29 19:58:48
categories: JavaScript
tags: [javascript]
---

<iframe src="https://player.vimeo.com/video/127548359" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>

<div class="not-on-video">
  <h2>Forms with Span tags</h2>
  <p>More form practice, now with spans.  Mastering forms is very useful for web developers.</p>
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
    <form>
      <div class="form-group">
        <label for="message">Message</label>
        <input type="text" class="form-control" id="message" placeholder="Message">
      </div>
      <div class="form-group">
        <label for="from">From</label>
        <input type="text" class="form-control" id="from" placeholder="From">
      </div>
      <div class="form-group">
        <label for="phone">Phone</label>
        <input type="text" class="form-control" id="phone" placeholder="Phone">
      </div>
      <button type="submit" class="btn btn-default">Submit</button>
    </form>
    <p>Message: <span class="message"></span> from: <span class="from"></span> Phone: <span class="phone"></span></p>
  </body>  
</html>

{% endhighlight %}


myscript.js

{% highlight JavaScript %}

$(document).ready(function(){
  $("form").on("submit", function(event){
    event.preventDefault();

    var message = $("input#message").val();
    var from = $("input#from").val();
    var phone = $("input#phone").val();

    $(".message").text(message);
    $(".from").text(from);
    $(".phone").text(phone);
  })
})



{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Make a new form with spans.</li>
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
