---
layout: page
title: "Numerical Tours"
description: "of Signal Processing"
header-img: "img/hokusai-0.jpg"
---

The <i>Numerical Tours of Signal Processing</i>, by [Gabriel Peyré](contact/), gather [Matlab](https://www.mathworks.com/products/matlab.html), [Python](https://www.python.org) and [Julia](https://julialang.org/) experiments to explore modern mathematical imaging sciences.
The tours are complemented by slides of courses detailing the theory and the algorithms.

{% for post in paginator.posts %}
<div class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
        <h2 class="post-title">
            {{ post.title }}
        </h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">
            {{ post.subtitle }}
        </h3>
        {% endif %}
    </a>
    <p class="post-meta">Posted by {{ post.author }} on {{ post.date | date: "%B %-d, %Y" }}</p>
</div>
<hr>
{% endfor %}

<!-- Pager -->
{% if paginator.total_pages > 1 %}
<ul class="pager">
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