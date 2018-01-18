---
title: Список проектов
---

# Книги

{% for book in site.data.books %}
  <div class="w3-card w3-light-gray w3-section">
    <div class="w3-container w3-yellow">
      <h2>{{ book.title }}</h2>
	</div>
	<div class="w3-container w3-padding">
	  {{ book.abstract }}
    </div>
	<div class="w3-ul w3-gray">
	  {% for link in book.links %}
	    <li>
		  <a href="{{ link.href }}">{{ link.name }} <i class="fa fa-external-link"></i></a>
		</li>
	  {% endfor %}
	</div>
  </div>
{% endfor %}
