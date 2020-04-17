{% include posts.liquid %}
# This is my blog. It runs on Jeykell. The Earth orbits the sun.
***
{% for post in posts %}
### {{ post.title }}
{% if post.exc %}
{{ post.exc }}
{% else %}
{{ post.body | truncatewords: 15 }}
{% endif %}
<p><img src="{{ post.er.img | default "_assets/images/users/noimg.png" }}" alt="" />{{ post.er.name | default "Annonymous" }}
***
{% endfor %}
<br/>
<br/>
<center>It looks like this is the end.</center>
