# Stream Archive
(Note: Older ones will probably be removed from twitch at some point, but I'll try to keep the youtube linkes alive.)

{% assign sorted = site.streams | reverse %}
{% for s in sorted %}
  <p>{{ s.content | markdownify }}
  	{% if s.twitch_id and s.twitch_id != "" and s.twitch_id != nil %}
  	<a target="_blank" rel="noopener noreferrer" href="https://www.twitch.tv/videos/{{s.twitch_id}}">
  		Twitch
    </a>
    {% endif %}
  	{% if s.youtube_id and s.youtube_id != "" and s.youtube_id != nil %}
  	<a target="_blank" rel="noopener noreferrer" href="https://www.youtube.com/watch?v={{s.youtube_id}}">
  		Youtube: <img src="http://img.youtube.com/vi/{{s.youtube_id}}/1.jpg"/>
    </a>
    {% endif %}
  {% if false %}
	![](http://img.youtube.com/vi/{{s.youtube_id}}/mqdefault.jpg)
  {% endif %}
  </p>
{% endfor %}
