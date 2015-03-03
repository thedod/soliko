---
layout: default-rtl
---

## {{site.description}}

אתר לתיעוד ומיגור תופעת החרוז הלבן-בז' בזמר העברי.

מסמך לא אנושי, אך מזעזע.
{% assign sortedsections = site.sections | sort: "title" %}
<ul id="toc">
  {% for s in sortedsections %}
  <li><a href="#{{s.url|slugify|replace:"-html",""}}">{{s.title}}</a>
  {% endfor %}
</ul>

<dl>
  {% for s in sortedsections %}
    <dt><h3 id="{{s.url|slugify|replace:"-html",""}}"><a href="#toc">{{ s.title }}</a></h3></dt>
    <dd>{{ s.content | markdownify }}</dd>
  {% endfor %}
</dl>

