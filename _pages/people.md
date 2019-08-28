---
layout: page
title: people
permalink: /people/
description: People who work with me.
---

{% comment %}

#### Hu Miao
Hu Miao works on CDW excitations




<p>Daniel Mazzone, Ph.D.(2017), Paul Scherrer Institut, Switzerland</p>
<p>Yao Shen, Ph.D.(2018), Fudan University, China</p>
<p>Jiaqi Lin, Ph.D. candidate,  Chinese Academy of Science</p>

<Strong>Alumni</Strong>:

<p>Derek Meyers, Assistant Professor, Oklahoma State University</p>
<p>Gilberto Fabbris, Scientist, Argonne National Laboratory</p>
{% endcomment %}


{% for project in site.people %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
