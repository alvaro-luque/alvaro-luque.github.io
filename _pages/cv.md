---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* M.S. in Physics of Complex Systems, IFISC (Mallorca, Spain), 2022-2023
* B.S. in Physics, University of Córdoba (Spain), 2017-2022

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Work experience
======

* Research assistant (03/2024-06/2025)
  * University of Córdoba, Department of Electrical Engineering and Automation 
  * Duties included: Merging pull requests

* Research Assistant (11/2021-05/2022)
  * University of Córdoba, TEP-215 research group (Physics for Renewable Energies)
  * Mathematical study of global irradiance model for agrivoltaic simulations. Python development of a simulation environment to estimate the irradiance on the soil in a user-defined photovoltaic power plant, aiming to study the viability of different crop species across a typical meteorological year.
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
