<!-- filepath: /c:/Users/ADMIN/Documents/1_Project/github-page/my-personal-website/index.md -->
---
layout: default
title: My Personal Website
---

{% include header.html %}

<main>
    <h2>Welcome to My Personal Website</h2>
    <p>This is the main entry point of my personal website built with Jekyll.</p>
    
    <h3>Recent Posts</h3>
    <ul>
        {% for post in site.posts %}
            <li>
                <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
                <span>{{ post.date | date: "%B %d, %Y" }}</span>
            </li>
        {% endfor %}
    </ul>
</main>

<footer>
    <p>&copy; {{ site.time | date: "%Y" }} My Personal Website</p>
</footer>

<script src="{{ '/assets/js/main.js' | relative_url }}"></script>