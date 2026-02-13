---
layout: page
title: Archive
permalink: /archive
---

# Archive

a good place to get lost for a while.

<ul>
  {% assign all_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in all_notes %}
    <li>
      {{ note.last_modified_at | date: "%d/%m/%Y" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
