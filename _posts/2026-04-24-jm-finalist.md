---
layout: post
title: Finalist for Best Paper Award
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


["Where A-B Testing Goes Wrong: How Divergent Delivery Affects What Online Experiments Cannot (and Can) Tell You About How Customers Respond to Advertising,"](){: class="link-primary" data-bs-toggle="modal" data-bs-target="#BraunSchwartz2025Modal"} is one of three  finalists for the 2025 AMA Marketing Science Institute/H. Paul Root Award.

<!--x-->

This award is given to the [_Journal of Marketing_](https://www.doi.org/10/nb5p){:target="_blank"} article that has made the most significant contribution to the advancement of the practice of marketing in a calendar year. It is cosponsored by the American Marketing Association and the Marketing Science Institute.

My co-author [Eric Schwartz](https://michiganross.umich.edu/faculty-research/faculty/eric-schwartz){:target="_blank"} (Michigan) and I congratulate the [winners of this award](https://www.ama.org/press-releases/neeraj-arora-ishita-chakraborty-and-yohei-nishimura-win-the-2025-ama-marketing-science-institute-h-paul-root-award/){:target="_blank"}:  Neeraj Arora, Ishita Chakraborty, and Yohei Nishimura, whose article on AI-Human Hybrids for Marketing Research is truly deserving.

Our article explains how **divergent delivery** may lead to your A-B tests not  telling you what you think they are.   It will be of interest to anyone who is considering using  ad platforms' freely available experimentation tools to compare the effectiveness of different creative elements (images, copy, messaging) in online advertising.  Divergent delivery occurs when a platform targets  different users to different ads, based on the content of those ads.  This makes it impossible for an advertiser to separate the effect of the ad from the effect from how an online platform's targeting algorithm decides which users see those ads.  We take the perspective of the practicing marketer who uses A-B test results to make strategic decisions based on which creative elements of ads are most effective.

 And there is a lot to say about how targeting policies, user heterogeneity, and data aggregation conspire to bias the magnitude, *and even the sign* of A-B test results. We provide evidence that platforms engage in divergent delivery even during the course of a seemingly randomized experiment.  And we also explain why platforms have no incentive to fix the problem.
