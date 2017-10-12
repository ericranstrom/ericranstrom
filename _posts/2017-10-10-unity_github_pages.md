---
title: "What we're doing"
date: 2017-10-10
categories:
  - General
tags:
  - about
  - jekyll
  - github pages
  - unity
---

{% capture fig_img %}
[![Foo](https://unity3d.com/profiles/unity3d/themes/unity/images/company/brand/logos/primary/unity-master-black.svg)](https://unity3d.com/profiles/unity3d/themes/unity/images/company/brand/logos/primary/unity-master-black.svg)
{% endcapture %}

{% capture fig_caption %}
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>{{ fig_caption | markdownify | remove: "<p>" | remove: "</p>" }}</figcaption>
</figure>

Hosting and Serving a unity webgl build from github pages.
Will update this post with instructions.
In the mean time, see the next post for a working example.
