---
layout: default
title: Kontakte
lang: de
permalink: /de/kontakte
---
<h1 class="title">{{ page.title }}</h1>
<div class="clear"></div>
<p>Phone: 00359 899 94 11 38</p>
{% if site.email %}
<p>E&ndash;mail: <span id="emailContainer"></span></p>
<script type="text/javascript">
  {% assign email = site.email|split: '@' %}
  var a = document.createElement('a');
  a.href = 'mailto:';
  a.href += '{{ email[0] }}';
  a.href += '@';
  a.href += '{{ email[1] }}';
  a.innerHTML = '{{ email[0] }}';
  a.innerHTML += '@';
  a.innerHTML += '{{ email[1] }}';
  document.getElementById('emailContainer').appendChild(a);
</script>
{% endif %}