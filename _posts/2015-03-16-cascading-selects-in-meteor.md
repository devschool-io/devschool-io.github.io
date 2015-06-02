---
layout: post
title:  "Cascading selects in Meteor"
date:   2015-03-16 16:29:48
categories: Meteor
tags: [meteor]
---
This is a quick cascading select with collections.  If you see any errors or recommendations please leave a comment.

{% highlight html %}
{% raw %}
#template html

<head>
  <title>cascading_select</title>
</head>

<body>
  <h1>Cascading select example</h1>
  {{> cascade}}
</body>

<template name="cascade">
  <select id="brands">
    <option value="">Select Brand</option>
    {{#each brands}}
      <option value="{{name}}">{{name}}</option>
    {{/each}}
  </select>
  <select id="models">
    <option value="">Select Model</option>
    {{#each models}}
      <option value="{{name}}">{{name}}</option>
    {{/each}}
  </select>
</template>
{% endraw %}
{% endhighlight %}

{% highlight javascript %}
#template js

Meteor.subscribe("Brands");
Meteor.subscribe("Models");

Template.cascade.helpers({
  brands: function(){
    return Brands.find();
  },
  models: function(){
    return Models.find({brand: Session.get("brandSelected")})
  }
});

Template.cascade.events({
  "change #brands": function(e){
    var brandSelected = $("#brands option:selected").val();
    Session.set("brandSelected", brandSelected);
  }
});

{% endhighlight %}

{% highlight javascript %}
# collections

Brands = new Meteor.Collection("Brands");

Models = new Mongo.Collection("Models");
{% endhighlight%}

{% highlight javascript %}
# publications

Meteor.publish("Brands", function(){
  return Brands.find();
});

Meteor.publish("Models", function(){
  return Models.find();
});
{% endhighlight %}

{% highlight javascript %}
# fixtures

if (Brands.find().fetch().length === 0){

  var brands = ["Audi", "BMW", "Chrysler"];

  var models = {
    "Audi": ["A3", "A4", "A5"],
    "BMW": ["3 Series", "4 series", "5 series"],
    "Chrysler": ["200", "300"]
  };

  for (var i = 0; i < brands.length; i++){
    Brands.insert({name: brands[i]});
    for (var j = 0; j < models[brands[i]].length; j++){
      Models.insert({name: models[brands[i]][j], brand: brands[i]})
    }
  }
}
{% endhighlight %}

<a href="https://github.com/devschool-io/cascading_select_meteor">Github repo </a>


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
