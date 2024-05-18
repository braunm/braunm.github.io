---
layout: page
title:  Published research and working papers
permalink: /papers/
---

<!-- CV and Google Scholar buttons -->

<div class="d-flex justify-content-around fg-info bg-light">
  <a class="btn btn-outline-primary" align="center" href="/cv/">CV</a>
  <a class="btn btn-outline-primary" align="center" href="https://scholar.google.com/citations?user=Rny0DIkAAAAJ&hl=en">Google Scholar</a>
</div>

{% assign allrefs=site.data.papers.references %}
{% assign wps = allrefs | where: "type", "working-paper" %}
<div class="citelist">
  <h2 class="type">Working papers</h2>
  <div class='row' data-masonry='{"percentPosition": true }'>
    {% for r  in wps %}
    <div class='col-sm-12 col-md-6 col-lg-4 col-xl-3 col-xxl-3 px-2 py-1 my-1'>
   {% include paper.html ref=r %}
   </div> <!-- column -->
    {% endfor %}
  </div> <!-- masonry row -->
</div> <!-- citelist -->

<hr>

<div class="citelist">
  <h2 class="type">Published articles</h2>
  <div class='row' data-masonry='{"percentPosition": true }'>
    {% assign articles = allrefs | where_exp: "allrefs", "allrefs.type contains 'article'" | sort:"year" %}
    {% for r in articles reversed %}
<div class='col-sm-12 col-md-6 col-lg-4 col-xl-3 col-xxl-3 px-2 py-1 my-1'>
    {% include paper.html  ref =r  %}
    </div>
    {% endfor %}

  </div>
</div>
