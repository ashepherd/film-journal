---
layout: page
permalink: /drafts/
title: Drafts
---
<table class="table is-fullwidth">
  <thead>
    <tr>
      <th>Post</th>
      <th>Date</th>
      <th>Category</th>
      <th>Authors</th>
    </tr>
  </thead>
  <tbody>
  {% for draft in site.drafts %}
    <tr>
      <th><a href="{{ draft.url }}">{{ draft.title }}</a></th>
      <td>{% if draft.date %}{{ draft.date | date_to_string: "ordinal", "US" }}{% else %}<span class="is-italic">not specified</span>{% endif %}</td>
      <td>{{ draft.category }}</td>
      <td>{{ draft.author | array_to_sentence_string }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>    
