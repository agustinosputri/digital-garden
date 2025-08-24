---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🪴

This is where I explore my ideas and share them publicly so others can read and provide feedback to help me improve my thinking.

Enjoy exploring my digital garden!

Thanks to Max, this digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

Also shoutout to Mike who shared on how to connect Obsidian [Guide available here](https://refinedmind.co/obsidian-jekyll-workflow).


<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
