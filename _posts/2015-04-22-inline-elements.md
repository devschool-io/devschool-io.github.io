---
layout: post
title:  "Inline Elements HTML"
date:   2015-04-21 16:29:48
categories: HTML
tags: [html-css]
---

<iframe src="https://player.vimeo.com/video/127847020" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>
<div class="not-on-video">
  <h2>Inline elements</h2> 
  <p>Inline elements do not add a new line after being defined.  It only occupies the space where it was defined.  For example a paragraph is NOT an inline element as it adds a new line after it.</p>

  <p>More info at <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elemente" target="_blank"> Mozilla</a></p>
</div>  


<h3>Hyperlink (a tag)</h3>

The text after ">" and before the closing tag "< /a>" is going to be displayed as the link text.
Remember to use target="_blank" if you want to open the link in a new window or tab.

{% highlight html %}

<a href="http://en.wikipedia.org/wiki/List_of_volcanoes_in_Guatemala">volcanoes in Guatemala.</a>

{% endhighlight %}

<h3>Image tag</h3>

Please note that image tags are self-closing. They do NOT require the closing tag </img>

{% highlight html %}

<img src="acatenango.jpg">

{% endhighlight %}

<h3>Span tag</h3>

Span tags are used when you want to modify the content inside the span tag.

{% highlight html %}

<li>Agua <span style="color:red">(active)</span><img src="agua.jpg"></li>

{% endhighlight %}


{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <title>Volcanoes in Guatemala</title>
  </head>
  <body>
    <p>Here you can find the list of all the <a href="http://en.wikipedia.org/wiki/List_of_volcanoes_in_Guatemala">volcanoes in Guatemala.</a></p>
    <p>Here are some examples</p>
    <ul>
      <li>Acatenango <img src="acatenango.jpg"></li>
      <li>Agua <span style="color:red">(active)</span><img src="agua.jpg"></li>
    </ul>
  </body>
</html>

{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Create a new web page.</li>
  <li>Add a link to your favorite website.</li>
  <li>Add an multiple images within a list (find anything you like) and add images to each list item.</li>
  <li>Add some text context and try to style it with a span.</li>
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