The `ensemble` branch allows splitting the text into `_sections/*.md`.
It's still a single page, but sometimes it's easier to maintain it this way.

Sections are sorted by title (made sense in this example), but if you want them sorted by filename,
Sort sections by `url` instead of `title`:

```
diff --git a/index.md b/index.md
index e05c5db..5aa1128 100644
--- a/index.md
+++ b/index.md
@@ -7,7 +7,7 @@ layout: default-rtl
 אתר לתיעוד ומיגור תופעת החרוז הלבן-בז' בזמר העברי.
 
 מסמך לא אנושי, אך מזעזע.
-{% assign sortedsections = site.sections | sort: "title" %}
+{% assign sortedsections = site.sections | sort: "url" %}
 <ul id="toc">
   {% for s in sortedsections %}
   <li><a href="#{{s.url|slugify|replace:"-html",""}}">{{s.title}}</a>
```

----

# סוליקו

A Hebrew (rtl) fork of
[Solo](http://solo.chibi.io) &mdash; a Jekyll theme that supports **single-page websites** only, but supports them well. Yes, it's responsive.

