# Journal
{% assign sorted = site.journal_entries | reverse %}
{% for j in sorted %}
  <p>{{ j.content | markdownify }}</p>
}
}
{% endfor %}
