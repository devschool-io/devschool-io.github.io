---
layout: post
title:  "Installing Bootstrap"
date:   2015-04-28 18:29:48
categories: HTML
tags: [html-css]
---

<iframe src="https://player.vimeo.com/video/127845311" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<br><br>

<h4>Installing Bootstrap</h4>
<p>Go over to <a href="http://www.getbootstrap.com" target="_blank">getbootstrap.com</a> and download bootstrap.  Extract the zip file and place the bootstrap.min.css file in your website's css folder.</p>

<figcaption>index.html</figcaption>

{% highlight html %}

<!DOCTYPE html>
<html>
  <head>
    <title>Using Bootstrap</title>
    <link rel="stylesheet" type="text/css" href="css/bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="css/styles.css">
  </head>
  <body>
    <p class="col-md-3">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
    <p class="col-md-3">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
  </body>
</html>


{% endhighlight %}

<figcaption>styles.css</figcaption>
{% highlight css %}

@media (min-width: 500px) and (max-width: 600px){
  p {
    color: red;
  }
}

{% endhighlight %}

<p>Try the following:</p>
<ul>
  <li>Create a new website and install bootstrap on it.  Remember to create a css folder and place bootstrap.min.css in it and link it on your index.html file.</li>
  <li>Add three paragraphs and try to make columns using the bootstrap grid system. (class="col-md-3")</li>
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