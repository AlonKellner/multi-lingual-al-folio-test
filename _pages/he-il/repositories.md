---
page_id: repositories
layout: page
permalink: /github/
title: גיטהאב
description: ערוך את `_data/repositories.yml` והחלף את רשימות ה-`github_users` וה-`github_repos` כדי להציג את פרופיל ה-github וה-Repo-ים שלך.
nav: true
nav_order: 4
default_liquid_style: # no style
header_liquid_style: 'dir=rtl style="text-align: right; font-family: Segoe UI"'
page_header_liquid_style: 'dir=rtl style="text-align: right; font-family: Segoe UI"'
footer_liquid_style: 'dir=rtl style="text-align: right; font-family: Segoe UI"'
---

## GitHub users

{% if site.data.repositories.github_users %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

## GitHub Repositories

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
