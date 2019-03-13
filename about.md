---
title: About
layout: page
---
![Profile Image]({{ site.url }}/{{ site.picture }})

<h2>Skills</h2>

<ul class="skill-list">
	<li>C/C++ </li>
	<li>ASM (i386 and ARM (Raspberry PI)</li>
	<li>C#</li>
	<li>VB6</li>
	<li>HTML</li>
	<li>Git</li>
	<li>PHP</li>
	<li>Python</li>
	<li>MySQL</li>

</ul>

<h2>Projects</h2>

<section class="list">
    {% for post in site.posts %}
        {% if post.projects %}
            <div class="item {% if post.star %}star{% endif %}">
                <a class="url" href="{% if post.externalLink %}{{ post.externalLink }}{% else %}{{ site.url }}{{ post.url }}{% endif %}">
                    <aside><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d %Y" }}</time></aside>
                    <h3 class="title">{{ post.title }}</h3>
                </a>
            </div>
        {% endif %}
    {% endfor %}
</section>
