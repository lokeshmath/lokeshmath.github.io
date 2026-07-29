---
title: "Teaching"
permalink: /teaching/
author_profile: true
layout: single
---

I teach the following courses at **Amity University Punjab, Mohali**. Click on a course title to access its materials (notes, assignments, and quizzes).

---

{% assign grouped_by_year = site.teaching | group_by: "year" %}
{% for year_group in grouped_by_year %}

## {{ year_group.name }}

  {% assign sorted_courses = year_group.items | sort: "semester_number" %}
  {% assign grouped_by_semester = sorted_courses | group_by: "semester_type" %}

  {% for semester_group in grouped_by_semester %}
    
### {{ semester_group.name }} Semester

    <ul>
      {% for course in semester_group.items %}
        <li>
          <strong><a href="{{ course.permalink }}">{{ course.title }}</a></strong> 
          – {{ course.course_code }}
        </li>
      {% endfor %}
    </ul>

  {% endfor %}

{% endfor %}
