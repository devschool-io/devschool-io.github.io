---
layout: post
title:  "Cascading, Classes and Ids"
date:   2015-04-23 18:29:48
categories: HTML
tags: [html-css]
---

<iframe src="https://player.vimeo.com/video/127847012" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>
<div class="not-on-video">
  <h4>Cascading</h4>
  <p>CSS rules applied to parent elements will be inherited by child elements.</p>
  <p>Classes and Ids are hooks that let us identify element tags.</p>
  <h4>Classes</h4>
  <p>An element can have many classes, classes are NOT unique.</p>
  <h4>Ids</h4>
  <p>An element can have only ONE ID, Id's are unique.</p>
</div>  



<figcaption>index.html</figcaption>
{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <title>Volcanoes in Guatemala</title>
    <link rel="stylesheet" type="text/css" href="css/styles.css"
  </head>
  <body>
    <p class="volcano">Here you can find the list of all the <a href="http://en.wikipedia.org/wiki/List_of_volcanoes_in_Guatemala">volcanoes in Guatemala.</a></p>
    <p>Here are some examples</p>
    <ul>
      <li class="volcano other-class" id="acatenango">Acatenango <img src="acatenango.jpg"></li>
      <li>Agua <span style="color:red">(active)</span><img src="agua.jpg"></li>
    </ul>
  </body>
</html>

{% endhighlight %}

<figcaption>styles.css</figcaption>
{% highlight css %}
li.volcano {
  font-weight: italic;
  color: red;
}

.other-class {
  font-size: 48px;
}

img {
  height: auto;
  width: 300px;
}

#acatenango {
  color: blue;
}

{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Add a class to your paragraph element and try to change the color, font-family and size.  Remember to use the class to apply the styling.</li>
  <li>Add ids to your list items (li) and change the font size, color and font-family (each list item has to look different).</li>
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