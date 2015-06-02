---
layout: post
title:  "Basic HTML"
date:   2015-04-21 16:29:48
categories: HTML
tags: [html-css]
---

<iframe src="https://player.vimeo.com/video/127847019" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>
<div class="not-on-video">
  <h2>HTML</h2>
  <p>HyperText Markup Language, commonly referred to as HTML, is the standard markup language used to create web pages. It is written in the form of HTML elements consisting of tags enclosed in angle brackets.</p>
  <br>
  <p>Source: Wikipedia</p>
</div>  

<br><br>

<figcaption>index.html</figcaption>
{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <title>Welcome to my page!</title>
  </head>
  <body>
    <p>Food I like:</p>
    <ul>
      <li>Pizza</li>
      <ul>
        <li>Ham and Cheese</li>
        <li>Mushrooms</li>
      </ul>
      <li>Hamburgers</li>
    </ul>
  </body>
</html>

{% endhighlight %}

<p>Try to get a text editor before you start. Either <a href="http://www.sublimetext.com/" target="_blank">Sublime Text</a> or <a href="http://www.atom.io" target="_blank">Atom</a> would work.</p>


<p>Try the following:</p>
<ul>
  <li>Create an html file called index.html</li>
  <li>Create a paragraph with any content inside of it. Open it in your browser to see the changes. If you see NO changes try to hit reload on the browser.</li>
  <li>Create a list of things you like (general things) and create sublists inside of each item for more precise things.</li>
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