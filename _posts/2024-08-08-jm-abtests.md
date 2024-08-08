---
layout: post
title: Another A-B testing paper
author: Michael Braun
category: Research
excerpt_separator: <!--x-->
---

{% assign paper=site.data.papers.references | where:   "id", "BraunSchwartz2024"  %}
{% assign jm = paper[0] %}
{% include modal.html rx=jm   %}


{% assign ABtest = site.data.papers.references | where:   "id", "BraunSchwartz2024"  %}
{% assign ab = ABtest[0] %}
{% include modal.html rx=ab   %}

Your A-B tests may not be telling you what you think they are!  Read about the dangers of **divergent delivery** in a my new paper, soon to be published in  the [_Journal of Marketing_](https://shortdoi.org/nb5p).

<!--x-->

 [Eric Schwartz](https://michiganross.umich.edu/faculty-research/faculty/eric-schwartz){:target="_blank"} (Michigan) and I have written ["Where A-B Testing Goes Wrong: How Divergent Delivery Affects What Online Experiments Cannot (and Can) Tell You About How Customers Respond to Advertising,"](){: class="link-primary" data-bs-toggle="modal" data-bs-target="#BraunSchwartz2024Modal"}, which last week was accepted for publication in the [Journal of Marketing](https://shortdoi.org/nb5p).


 This article will be of interest to anyone who is considering using  ad platforms' freely available experimentation tools to compare the effectiveness of different creative elements (images, copy, messaging) in online advertising.  Divergent delivery occurs when a platform targets  different users to different ads, based on the content of those ads.  This makes it impossible for an advertiser to separate the effect of the ad from the effect from how an online platform's targeting algorithm decides which users see those ads.  We take the perspective of the practicing marketer who uses A-B test results to make strategic decisions based on which creative elements of ads are most effective.

 And there is a lot to say about how targeting policies, user heterogeneity, and data aggregation conspire to bias the magnitude, *and even the sign* of A-B test results. We provide evidence that platforms engage in divergent delivery even during the course of a seemingly randomized experiment.  And we also explain why platforms have no incentive to fix the problem.


#####  Here's the full abstract of the paper:

>  Abstract

{{  paper[0].abstract }}
