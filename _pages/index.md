---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my fieldnotes <3 💐

<p style="padding: 3em 1em; background: #e9f4be; border-radius: 4px;">
  if my writing is an ecosystem of interconnected practices that feed into each other, like the different flora and fauna in a garden, then this is me, giving you a flower.  
</p>
 
<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%d/%m/%Y" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
