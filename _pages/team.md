---
title: "LIPS Lab - Team"
layout: gridlay
excerpt: "LIPS Lab: Team members"
sitemap: false
permalink: /team/
---

<style>
.team-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 40px;
  margin: 40px 0;
}

.team-member {
  text-align: center;
  width: 200px;
}

.team-member-photo {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  object-fit: cover;
  margin: 0 auto 15px;
  display: block;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.team-member-name {
  font-size: 18px;
  font-weight: bold;
  margin: 10px 0 5px;
  color: #333;
}

.team-member-role {
  font-size: 14px;
  color: #666;
  font-style: italic;
  line-height: 1.4;
}

.section-title {
  font-size: 28px;
  font-weight: bold;
  margin: 40px 0 20px;
  padding-bottom: 10px;
  border-bottom: 2px solid #e0e0e0;
}
</style>

<div markdown="0">
<h1 class="section-title">Members</h1>

<div class="team-grid">
{% for member in site.data.team_members %}
  <div class="team-member">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="team-member-photo" alt="{{ member.name }}" />
    <div class="team-member-name">{{ member.name }}</div>
    <div class="team-member-icons" style="margin: 10px 0; display: flex; justify-content: center; gap: 15px;">
      {% if member.linkedin %}
      <a href="{{ member.linkedin }}" target="_blank" style="color: #0077b5; text-decoration: none;" title="LinkedIn">
        <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
      </a>
      {% endif %}
      {% if member.scholar %}
      <a href="{{ member.scholar }}" target="_blank" style="color: #4285f4; text-decoration: none;" title="Google Scholar">
        <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 24a7 7 0 1 1 0-14 7 7 0 0 1 0 14zm0-24L0 9.5l4.838 3.94A8 8 0 0 1 12 9a8 8 0 0 1 7.162 4.44L24 9.5z"/></svg>
      </a>
      {% endif %}
      {% if member.website %}
      <a href="{{ member.website }}" target="_blank" style="color: #333; text-decoration: none;" title="Personal Website">
        <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
      </a>
      {% endif %}
    </div>
    <div class="team-member-role">{{ member.info }}</div>
  </div>
{% endfor %}
</div>
</div>


<!--
## Master and Bachelor Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
-->


<div markdown="0">
<h1 class="section-title">Alumni</h1>

<div class="team-grid">
{% for member in site.data.alumni_members %}
  <div class="team-member">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="team-member-photo" alt="{{ member.name }}" />
    <div class="team-member-name">{{ member.name }}</div>
    <div class="team-member-icons" style="margin: 10px 0; display: flex; justify-content: center; gap: 15px;">
      {% if member.linkedin %}
      <a href="{{ member.linkedin }}" target="_blank" style="color: #0077b5; text-decoration: none;" title="LinkedIn">
        <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
      </a>
      {% endif %}
      {% if member.scholar %}
      <a href="{{ member.scholar }}" target="_blank" style="color: #4285f4; text-decoration: none;" title="Google Scholar">
        <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 24a7 7 0 1 1 0-14 7 7 0 0 1 0 14zm0-24L0 9.5l4.838 3.94A8 8 0 0 1 12 9a8 8 0 0 1 7.162 4.44L24 9.5z"/></svg>
      </a>
      {% endif %}
      {% if member.website %}
      <a href="{{ member.website }}" target="_blank" style="color: #333; text-decoration: none;" title="Personal Website">
        <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
      </a>
      {% endif %}
    </div>
    <div class="team-member-role">{{ member.info }}<br>{{ member.duration }}</div>
  </div>
{% endfor %}
</div>
</div>

<!--
## Former visitors, BSc/ MSc students
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Master students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>
-->

<!--
## Administrative Support
<a href="mailto:admin@memphis.edu">Administrative Contact</a> is helping us with administration.
-->
