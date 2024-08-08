---
layout: post
title: New paper on using A-B tests for academic research
author: Michael Braun
category: Research
excerpt_separator: <!--x-->
---

{% assign paper=site.data.papers.references | where:   "id", "BraunDeLanghe2024"  %}
{% assign jcr = paper[0] %}
{% include modal.html rx=jcr   %}


{% assign ABtest = site.data.papers.references | where:   "id", "BraunSchwartz2024"  %}
{% assign ab = ABtest[0] %}
{% include modal.html rx=ab   %}


Online A-B tests using targeted ad platforms are  not randomized experiments.  That can put the internal validity of your study in doubt.  This is the subject of my new paper, published in  the _Journal of Consumer Research_.


<!--x-->

In ["Leveraging Digital Advertising Platforms for Consumer Research,"](){: class="link-primary" data-bs-toggle="modal" data-bs-target="#BraunDeLanghe2024Modal"}  [Bart De Langhe](https://www.vlerick.com/en/find-faculty-and-experts/bart-de-langhe/){:target="_blank"}  (Vlerick),
[Stefano Puntoni](https://marketing.wharton.upenn.edu/profile/puntoni/){:target="_blank"}  (Wharton),  [Eric Schwartz](https://michiganross.umich.edu/faculty-research/faculty/eric-schwartz){:target="_blank"} (Michigan), and I explain why experiments using digital advertising platforms are likely not answering the question you are asking.


Many online advertising platforms provide tools to help researchers conduct experiments on the relative effectiveness of ads.  But  platforms target different users to different ads, based on the content of those ads.  This creates a confound that makes it impossible to separate the effect of the ad from the effect from how an online platform's targeting algorithm decides which users see those ads. As a result,  which of the platform's users are included in the experiment, and how experimental subjects are selected to be exposed to each treatment, are __not randomized__.

Our paper lays out this problem from the perspective of academic researchers who may be considering conducting field experiments using these tools.  We want these researchers to understand the trade-offs between the convenience of only A-B testing and the threats to internal validity that result from ad targeting.  In this paper, we provide a set of guidelines for researchers (and editors) to follow when determining whether certain online experimental designs are appropriate, and how much weight should be placed on the resulting inferences.

Eric and I also have  a <a class="link-primary" data-bs-toggle="modal" data-bs-target="#BraunSchwartz2024Modal"> complementary paper </a>  that goes into some quantitative  detail about how   _divergent delivery_ of different ads to different users generates bias in A-B test results. This paper takes the perspective of the practicing marketer who uses A-B test results to make strategic decisions based on which creative elements of ads are most effective.



#####  Here's the full abstract of the _JCR_ paper:

>  Abstract



{{  paper[0].abstract }}
