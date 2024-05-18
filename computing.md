---
layout: page
title: Computing
permalink: /computing/
---



## R packages

I am the author and current maintainer of three packages for the R statistical programming language.  I also have a library of code snippets for R, emacs, and LaTeX that I will post from time to time, as I clean them up for public review.


{% assign Rpacks= site.data.computing.packages | where: "type", "R-package" %}

<div class='row' data-masonry='{"percentPosition": true }'>
{% for pack in Rpacks %}
{% assign popID =  pack.name  | append: "pop"  %}
<div class='col-sm-12 col-md-4 col-lg-4 px-2 py-1 my-1'>
    <div class="paper-card" >
        <div class="d-flex justify-content-apart">
            <span class="col-3 text-left year">{{pack.version}}</span>
            <span class="col-9 text-right topic">{{pack.type }}</span>
        </div>
            <a class='title stretched-link'  href='{{pack.website | prepend: "https://"}}'>{{pack.name }} </a>
      <span class="body" >{{pack.description}}</span>
    </div >
  </div>
{% endfor %}
</div>


## Posts about computing

Excerpts of some computing-related blog posts. Click for the full post.

{% assign posts = site.posts | where: "category", "Computing" %}
<div class='row' data-masonry='{"percentPosition": true }'>
  {% for post in posts %}
  {% assign popID = post.name  | append: "pop"  %}
  <div class='col-sm-12 col-lg-6 col-xl-4 px-2 py-1 my-1'>
    <div class="paper-card" data-bs-toggle="modal"  data-bs-target="{{ popID | prepend: "#" }}">
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
{% endfor %}
</div>
