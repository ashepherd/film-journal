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
    </tr>
  </thead>
  <tbody>
  {% for draft in site.drafts %}
    <tr>
      <th><a href="{{ draft.url }}">{{ draft.title }}</a></th>
      <td>{% if draft.date %}{{ draft.date | date_to_string: "ordinal", "US" }}{% else %}<span class="is-italic">not specified</span>{% endif %}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>    
