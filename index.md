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

<div class="github-fork-ribbon-wrapper right fixed" style="width: 150px;height: 150px;position: fixed;overflow: hidden;top: 0;z-index: 9999;pointer-events: none;right: 0;"><div class="github-fork-ribbon" style="position: absolute;padding: 2px 0;background-color: #333;background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.15));-webkit-box-shadow: 0 2px 3px 0 rgba(0, 0, 0, 0.5);-moz-box-shadow: 0 2px 3px 0 rgba(0, 0, 0, 0.5);box-shadow: 0 2px 3px 0 rgba(0, 0, 0, 0.5);z-index: 9999;pointer-events: auto;top: 42px;right: -43px;-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);-ms-transform: rotate(45deg);-o-transform: rotate(45deg);transform: rotate(45deg);"><a href="https://github.com/thedod/soliko/tree/ensemble#readme" style="font: 700 13px &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif;color: #fff;text-decoration: none;text-shadow: 0 -1px rgba(0, 0, 0, 0.5);text-align: center;width: 200px;line-height: 20px;display: inline-block;padding: 2px 0;border-width: 1px 0;border-style: dotted;border-color: rgba(255, 255, 255, 0.7);">Fork me on GitHub</a></div></div>

