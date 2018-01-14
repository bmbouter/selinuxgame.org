---
layout: page
title: Tutorials
---

All of the tutorials below are designed to teach SELinux commands used in the
scenarios. These are self-guided and provide the solution with the exercise.

Each of these can be tested with the `tutorials` box. Load it with
`vagrant up tutorials`.

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
{% for tutorial in site.tutorials %}
    <tr>
      <td><a href="{{ site.baseurl }}{{ tutorial.url }}">{{ tutorial.title }}</a></td>
      <td>{{ tutorial.description }}</td>
    </tr>
{% endfor %}
  </tbody>
</table>
