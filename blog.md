---
layout: default
title: Blog
permalink: /blog/
---

From time to time I will post thoughts on various subjects.


{% for cat in site.categories  %}
<h4> {{ cat[0]  }} </h4>
<div class='row' data-masonry='{"percentPosition": true }'>
{% for post in cat[1] %}
 <div class='col-sm-6  col-lg-4 col-xl-4 px-2 py-1 my-1'>
<div class="paper-card" >
      <div class="d-flex justify-content-apart">
        <span class="col-6 text-left year">{{post.date | date_to_string }}</span>
        <span class="col-6 text-right topic">{{post.category }}</span>
     </div>
      <a  class="title stretched-link" href="{{ post.url }}">{{post.title }} </a>
      <div class="body">
{{ post.excerpt }}
</div>
</div>
</div>
{%  endfor  %}
</div>

{% endfor %}
