---
layout: main
title: Publications
---

<div>
{%- for entry in site.data.publications -%}
<h2>{{ entry[0] }}</h2>
<ol>
    {%- for x in entry[1] -%}
        <li>
        {{ x.authors | join: ', ' }}. 
        {{ x.title }}.
        {% if x.where %} <em>{{ x.where }}</em>,{% endif %}
        {% if x.vol %} {{ x.vol }}{% if x.num %}({{ x.num }}){% endif %}:{% endif %}{% if x.pages %}{{ x.pages }},{% endif %} 
        {{ x.year }}.
        {% if x.doi %} <abbr>doi</abbr> <a href="http://dx.doi.org/{{ x.doi }}">{{ x.doi }}</a>.{% endif %}
        {% if x.regno %} <span><abbr>reg. no.</abbr>&nbsp;{{ x.regno }}.</span>{% endif %}
        {% if x.lang %} Made with {{ x.lang }}.{% endif %}
        {% if x.source %} <a href="{{ x.source }}">Source</a>.{% endif %}
        {% if x.licence %} {{ x.license }}.{% endif %}
        {% if x.note %} {{ x.note }}.{% endif %}
        </li>  
    {%- endfor -%}
</ol>
{%- endfor -%}  
</div>