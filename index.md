---
layout: default
pic1: /assets/images/Braun_2018_with_tie_square.png
pic2: /assets/images/MB_Fox4_2015_sq3.png
pic3: /assets/images/MB_MDC_2018.png
permalink: /
---


<div class="row g-0 justify-content-center">
  <img class='col-4' src='{{ page.pic1 }}'>
  <img class='col-4' src='{{ page.pic2 }}'>
  <img class="col-4" src='{{ page.pic3 }}'>
</div>




  <div class=" container-fluid card shadow my-4">
    <span class="topic">Michael Braun</span>
    <div class="body">
      <div class="d-flex justify-content-evenly">
        <div class="col-7  my-1">
          <ul>
            <li class="list-group-item">Corrigan Reserach Professor</li>
            <li class="list-group-item">Associate Professor of Marketing</li>
            <li class="list-group-item">SMU Cox School of Business</li>
            <li class="list-group-item">Southern Methodist University</li>
          </ul>
        </div>
        <div class="col-5  my-1 text-center">
          <a class="btn btn-outline-primary mx-1" href="/cv/">CV</a>
          <a class="btn btn-outline-primary mx-1" href="/papers/">Papers</a>
        </div>
      </div>
    </div>
  </div>






<div class="row" data-masonry='{"percentPosition": true }'>
  {% assign cards=site.data.frontcards.cards %}  <!-- |sort: "order" % } -->
  {% for card in cards %}
  <div class="col-sm-12 col-md-6 col-lg-4 col-xl-4 py-1 my-1">
    <div class="card shadow">
      <h5 class="topic"> {{ card.topic }} </h5>
      <div class="body">
        <ul>
          {% for line in card.body.items %}
          <li> {{ line }} </li>
          {% endfor %}
        </ul>
      </div>
    </div>
  </div>
  {% endfor %}
</div>




<div class="my-3">
  <h4>News</h4>


<div class='row' data-masonry='{"percentPosition": true }'>
  {% for post in site.posts %}
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



</div>







<!-- I am currently the Corrigan Research Professor, and Associate Professor of Marketing, at the Cox School of Business of Southern Methodist University. -->

<!-- My research interests include: -->

<!-- - Statistical methods for analyzing marketing data (broadly defined) -->
<!-- - Modeling customer value and retention -->
<!-- - Measuring online advertising effectiveness -->
