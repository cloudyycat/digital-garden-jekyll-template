---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my fieldnotes <3 💐

<p style="padding: 3em 1em; background: #e9f4be; border-radius: 4px;">
  If my writing is an ecosystem of interconnected practices that feed into one another, like the different flora and fauna that comprise a garden, then website is me, lovingly giving you a flower. Please feel free to find a shady spot and stay for a while. 

  This site is very much an experiment, and is forever in progress (much like a real garden), so imperfections are welcome and embraced. 
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
