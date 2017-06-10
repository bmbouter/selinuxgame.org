---
layout: page
title: Leaderboard
---
## Top Players

{% assign players_sorted_by_count = (site.data.players | sort: 'count') | reverse %}

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th># Lessons Completed</th>
    </tr>
  </thead>
  <tbody>
{% for player in players_sorted_by_count %}
    <tr>
      <td>{{ player.nick }}</td>
      <td>{{ player.scenarios | number_of_words }}</td>
    </tr>
{% endfor %}
  </tbody>
</table>
