---
layout: page
title: Archive
permalink: /archive.html
---
<article class="page">

  <div class="entry" style="display: inline-block">

    {% for post in site.posts %}
      {% if post.removed %}

        <ul style="list-style-type: none; display: flex;">
          <li><a href="{{ site.baseurl }}{{ post.url }}" id="removed" style="float: left; font: 18px/1.4 Merriweather-R;"> {{ post.title }}  </a><p style="float: right; margin: 0px 0"> &nbsp; ({{ post.date | date: '%m/%d/%Y' }})</p></li>
        </ul>

      {% else %}

        <ul style="list-style-type: none; display: flex;">
          <li><a href="{{ site.baseurl }}{{ post.url }}" style="float: left; font: 18px/1.4 Merriweather-R;"> {{ post.title }}  </a><p style="float: right; margin: 0px 0"> &nbsp; ({{ post.date | date: '%m/%d/%Y' }})</p></li>
        </ul>

      {% endif %}
    {% endfor %}

  </div>

</article>
