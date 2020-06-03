---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Home
permalink: 
---

<ul class="post-list">
    <!-- <h1>Latest Post</h1> -->
    {% for post in site.posts limit:1 %}
        <li>
            <h2>
                <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
            </h2>
            <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        </li>

        {{ post.content }}
    {% endfor %}

    {%- if site.posts > 1 -%}
        <h1>Recent Posts</h1>
        {% for post in site.posts offset:1 %}
            <li>
                <h2>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                </h2>
                <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
            </li>

            {{ post.content }}
        {% endfor %}
    {% endif %}
</ul>
