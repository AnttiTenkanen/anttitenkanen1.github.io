---
layout: page
title: Brews
subtitle: Some of my best homebrews, with instructions!
---

<!-- tämä oli jotain paginatorturhuutta joka oli jäänyt tänne eikä varmaan toimi --> 
<div class="posts-list">
  {% for post in paginator.posts %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	  <h2 class="post-title">{{ post.title }}</h2>
	
	  {% if post.subtitle %}
	  <h3 class="post-subtitle">
	    {{ post.subtitle }}
	  </h3>
	  {% endif %}  
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: "%B %-d, %Y" }}
    </p>
  
    <div class="post-entry">
      {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
	  <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
    </div>
  
   </article>
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}


<head>

<!-- JAKONAPIT --> 
<div style="text-align:center">
<span class='st_sharethis_large' displayText='ShareThis'></span>
<span class='st_facebook_large' displayText='Facebook'></span>
<span class='st_twitter_large' displayText='Tweet'></span>
<span class='st_reddit_large' displayText='Reddit'></span>
<span class='st_whatsapp_large' displayText='WhatsApp'></span>
<span class='st__large' displayText=''></span>
</div>

<!-- JAKONAPPIKOODI --> 
<script type="text/javascript">(function(){window.switchTo5x=false;var e=document.createElement("script");e.type="text/javascript";e.async=true;e.onload=function(){try{stLight.options({publisher: "5bb2ce9e-03b5-4a38-abaa-4e93c9f44a3c-a51c", doNotHash: false, doNotCopy: false, hashAddressBar: true});}catch(e){}};e.src=("https:" == document.location.protocol ? "https://ws" : "https://ws") + ".sharethis.com/button/buttons.js";var s = document.getElementsByTagName("script")[0];s.parentNode.insertBefore(e, s);})();</script>

</head>
