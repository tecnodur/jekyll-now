---
published: true
description: Simple explanation 
title: Adding a share reddit button
date: 2017-06-24 21:15:00
share: true
layout: post
comments: true
publish: true
tags:
  - customizations
  - jekyll
---
## Adding the share Reddit option

So, i wanted to add the share Reddit button.
The theme as facebook, twitter, google+, linkdin, instagram and email, share buttons.
I don't need the instagram one, but i'd like to have a Reddit one. 
So in the file _includes/share.html , i've remove the part about instagram, and i've added
{% highlight html %}
{% raw %}
    {% if site.share.reddit %}
    <li class="share-reddit">
      <a href="https://www.reddit.com/submit?url={{ page.url | absolute_url }}&title={{ page.title }}" class="btn" title="{{ site.data.ui-text[site.locale].share_on_label }} Reddit">
       <span class="fa-stack fa-lg">
         <i class="fa fa-circle-thin fa-stack-2x"></i>
         <i class="fa fa-reddit fa-stack-2x"></i>
       </span>
      </a>
    </li>
    {% endif %}
{% end raw %}
{% endhighlight xml %}
