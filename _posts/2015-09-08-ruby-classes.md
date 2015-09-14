---
layout: post
title:  "Classes in Ruby"
date:   2015-09-08 21:58:48
categories: Ruby

tags: [ruby]
---

<!-- <iframe src="https://player.vimeo.com/video/127754068" width="1000" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
 -->

<br><br>

<div class="not-on-video">
  <h2>Classes and Objects</h2>
  <p>A class is the blueprint from which individual objects are created.</p>
  <p>Everything is an object in Ruby and objects are instances of a class.  Think of a class being a mold of something and a object is the thing that was created using that mold. An object is also know as an instance of a class.</p>
</div>

<h4>How to know to what class an object belongs to? Use the class() method on the object.</h4>

{% highlight ruby %}

123.class()

# Fixnum

1.23.class()

# Float

"123".class()

# String

[1, 2, 3].class()

# Array


{% endhighlight %}

<h4>Defining our own classes.</h4>

person.rb
{% highlight ruby %}

class Person
  # Important comment: The initialize method automatically runs whenever an instance of any class is created.
  def initialize(name)
    @name = name
  end
end


# adding your own methods to the class

class Person
  def initialize(name)
    @name = name
    @from = "Guatemala"
  end

  def greet
    return "Hello my name is #{@name} and I am from #{@from}"
  end
end

# adding getter and setter methods

class Person
  def initialize(name)
    @name = name
    @from = "Guatemala"
  end

  def name
    @name
  end

  def name=(string)
    @name = string
  end

  def greet
    return "Hello my name is #{@name} and I am from #{@from}"
  end
end

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
