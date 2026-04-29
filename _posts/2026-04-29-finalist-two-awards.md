---
layout: post
title: Finalist for Two Best Paper Awards
author: Michael Braun
category: Research
excerpt_separator: <!--x-->
---

{% assign paper=site.data.papers.references | where:   "id", "BraunSchwartz2025"  %}
{% assign jm = paper[0] %}
{% include modal.html rx=jm   %}


{% assign ABtest = site.data.papers.references | where:   "id", "BraunSchwartz2025"  %}
{% assign ab = ABtest[0] %}
{% include modal.html rx=ab   %}


["Where A-B Testing Goes Wrong: How Divergent Delivery Affects What Online Experiments Cannot (and Can) Tell You About How Customers Respond to Advertising,"](){: class="link-primary" data-bs-toggle="modal" data-bs-target="#BraunSchwartz2025Modal"} is a finalist for two best paper awards at the _Journal of Marketing_.

<!--x-->

The AMA Marketing Science/H. Paul Root Award recognizes the [_Journal of Marketing_](https://www.doi.org/10/nb5p){:target="_blank"} article that has made the most significant contribution to the advancement of the practice of marketing in a calendar year (2025). It is cosponsored by the American Marketing Association and the Marketing Science Institute.

The Shelby D. Hunt/Harold H. Maynard Award recognizes the  [_Journal of Marketing_](https://www.doi.org/10/nb5p){:target="_blank"}  article published in the last calendar year (2025) that has made the most significant contribution to marketing theory.

Each award honors only three finalists.

This article explains how **divergent delivery** may lead to your A-B tests not  telling you what you think they are.   It will be of interest to anyone who is considering using  ad platforms' freely available experimentation tools to compare the effectiveness of different creative elements (images, copy, messaging) in online advertising.  Divergent delivery occurs when a platform targets  different users to different ads, based on the content of those ads.  This makes it impossible for an advertiser to separate the effect of the ad from the effect from how an online platform's targeting algorithm decides which users see those ads.  We take the perspective of the practicing marketer who uses A-B test results to make strategic decisions based on which creative elements of ads are most effective.

 And there is a lot to say about how targeting policies, user heterogeneity, and data aggregation conspire to bias the magnitude, *and even the sign* of A-B test results. We provide evidence that platforms engage in divergent delivery even during the course of a seemingly randomized experiment.  And we also explain why platforms have no incentive to fix the problem.
