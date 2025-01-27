---
layout: page
title: Homework
img: code.png # Add image post (optional)
permalink: homework
sidebar: true
---

---

Unless otherwise noted, homework assignments will be posted here on Wednesday afternoons, and are due the following Wednesday at 12:30pm (half an hour before class).

Don't forget that there will also be occasional reading discussions on Canvas.

To submit your work, please email a PDF to Kian (kian@caltech.edu) with the subject line "[Bi/Ge 105] HW # - FirstName LastName", substituting the assignment number and your actual name.


<table>
<tr>
<th> <b>Homework</b></th>
<th> <b> Problem Set </b></th>
<th> <b>Associated Files</b></th>
<th> <b> Due Date</b> </th>
</tr>
{% for hwk in site.data.homework %}
<tr>
<td> {{hwk.number}} </td>
<td> <a href="http://www.rpgroup.caltech.edu/BiGe105_evolution/assets/hwk/{{hwk.pset}}"> Problem Set </a></td>
{% if hwk.data %}
{% for dataset in hwk.data %}
<td> <a href="http://www.rpgroup.caltech.edu/BiGe105_evolution/data/{{dataset.link}}">{{dataset.name}}</a></td>
{% endfor %}
{% else %}
<td> -- </td>
{% endif %}
<td> {{hwk.due_date}} </td>
{% if hwk.solutions %}
<td> <a href="https://rpdata.caltech.edu/courses/BiGe105_evolution/assets/solutions/{{hwk.solns}}">Solutions</a></td>
{% endif %}
</tr>
{%endfor%}
</table>
