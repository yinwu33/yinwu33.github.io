---
permalink: /
title: "Yin Wu"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<section class="home-hero">
  <p class="home-kicker">ADAS / AD verification and validation</p>
  <p class="home-lead">
    I am a Ph.D. researcher at CARIAD SE and Karlsruhe Institute of Technology, working on data-driven verification and validation for ADAS and autonomous driving. My research focuses on cross-country release validation, scenario identification, virtual scenario generation, and ODD coverage.
  </p>
  <div class="home-actions" aria-label="Contact links">
    <a class="btn btn--primary" href="mailto:yinwu.life@gmail.com">Email</a>
    <a class="btn" href="https://scholar.google.com/citations?user=Va5MksQAAAAJ&amp;hl=en">Google Scholar</a>
  </div>
</section>

<section class="home-section" id="research">
  <h2>Research</h2>
  <p>
    My work combines scenario generation, scenario mining, multi-sensor perception, reinforcement learning planners, and ADAS system integration to make validation more efficient and more representative across operating domains.
  </p>
  <div class="home-chip-list">
    <span class="home-chip">Scenario generation</span>
    <span class="home-chip">Scenario mining</span>
    <span class="home-chip">ADAS / AD validation</span>
    <span class="home-chip">ODD coverage</span>
    <span class="home-chip">Multi-sensor perception</span>
    <span class="home-chip">Agentic AI</span>
  </div>
</section>

<section class="home-section" id="cv">
  <h2>Education</h2>
  <div class="home-timeline">
    <article class="home-entry">
      <div class="home-entry__head">
        <h3>Karlsruhe Institute of Technology, Ph.D.</h3>
        <span>09/2023 - Present</span>
      </div>
      <p class="home-meta">Data-driven verification and validation in ADAS/AD</p>
      <p>Research focus: cross-country ADAS release validation, scenario identification, and virtual scenario generation for ODD coverage.</p>
    </article>
    <article class="home-entry">
      <div class="home-entry__head">
        <h3>Karlsruhe Institute of Technology, M.Sc.</h3>
        <span>10/2019 - 03/2023</span>
      </div>
      <p class="home-meta">Mechatronics and Information Technology, Robotics</p>
    </article>
    <article class="home-entry">
      <div class="home-entry__head">
        <h3>Beijing Institute of Technology, B.Sc.</h3>
        <span>09/2015 - 07/2018</span>
      </div>
      <p class="home-meta">Vehicle Engineering</p>
    </article>
  </div>
</section>

<section class="home-section" id="experience">
  <h2>Experience</h2>
  <div class="home-timeline">
    <article class="home-entry">
      <div class="home-entry__head">
        <h3>CARIAD SE, Germany</h3>
        <span>09/2023 - Present</span>
      </div>
      <p class="home-meta">Ph.D. Student, Scenario and Testing Department</p>
      <ul>
        <li>Research and project work in data-driven ADAS/AD verification and validation.</li>
        <li>Contributed to PoCs for an LLM-based scenario agentic editor and LLM-based test case generation.</li>
        <li>Supported corner case detection from bus data.</li>
      </ul>
    </article>
    <article class="home-entry">
      <div class="home-entry__head">
        <h3>LiangDao GmbH, Germany</h3>
        <span>04/2022 - 08/2023</span>
      </div>
      <p class="home-meta">Computer Vision Algorithm Engineer, 05/2023 - 08/2023</p>
      <ul>
        <li>Developed an online HD map generation network using LiDAR point clouds.</li>
        <li>Built and maintained GitLab CI/CD pipelines for production deployment.</li>
      </ul>
      <p class="home-meta">Master Thesis, 08/2022 - 03/2023</p>
      <ul>
        <li>Thesis: Fusion of Multi-Information to Improve Object Detection Results for LiDAR Point Clouds.</li>
        <li>Developed a sensor fusion and object tracking system for autonomous driving.</li>
      </ul>
      <p class="home-meta">Intern, Field Application Engineering, 04/2022 - 07/2022</p>
      <ul>
        <li>Assembled and integrated edge-computing LiDAR systems.</li>
        <li>Deployed hardware solutions at customer sites and developed evaluation software for LiDAR system performance.</li>
      </ul>
    </article>
    <article class="home-entry">
      <div class="home-entry__head">
        <h3>Karlsruhe Institute of Technology, Germany</h3>
        <span>07/2021 - 03/2022</span>
      </div>
      <p class="home-meta">Student Assistant, ADAS Integration, 07/2021 - 03/2022</p>
      <ul>
        <li>Built a multi-sensor data collection system integrating LiDAR, cameras, and GNSS/IMU sensors with ROS-based software.</li>
        <li>Worked on sensor calibration and time synchronization.</li>
      </ul>
      <p class="home-meta">Tutor, Optimization and Dynamic System, 12/2021 - 03/2022</p>
      <p>Tutored exercise classes and provided MATLAB programming guidance.</p>
    </article>
  </div>
</section>

<section class="home-section" id="publications">
  <h2>Publications</h2>
  {%- comment -%}
    Generated from _publications/*.md with `homepage: true`, newest `date` first.
    Fields: title, venue, date, authors, pdf (arXiv PDF link); optional: cover, award, author_note.
    Papers with `layout: project` get a "Project Page" link; the others link to arXiv.
  {%- endcomment -%}
  {%- assign home_pubs = site.publications | where_exp: "pub", "pub.homepage" | sort: "date" | reverse -%}
  {%- for pub in home_pubs %}
  {%- if pub.layout == "project" -%}{%- assign pub_link = pub.url | relative_url -%}{%- else -%}{%- assign pub_link = pub.paperurl | default: pub.pdf -%}{%- endif %}
  <article class="home-publication{% if pub.cover %} home-publication--with-media{% endif %}">
    {%- if pub.cover %}
    <a class="home-publication__media" href="{{ pub_link }}" aria-label="{{ pub.title | escape_once }}">
      <img src="{{ pub.cover | relative_url }}" alt="{{ pub.cover_alt | default: pub.title | escape_once }}" loading="lazy">
    </a>
    {%- endif %}
    <div class="home-publication__body">
      <h3><a href="{{ pub_link }}">{{ pub.title }}</a></h3>
      {%- if pub.authors %}
      <p class="home-authors">{% for author in pub.authors %}{% assign author_name = author | remove: "*" %}{% if author_name == site.author.name %}<strong class="home-me">{{ author }}</strong>{% else %}{{ author }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}{% if pub.author_note %} <span class="home-author-note">({{ pub.author_note }})</span>{% endif %}</p>
      {%- endif %}
      <p class="home-meta">{{ pub.venue }}{% if pub.award %} <span class="home-award">{{ pub.award }}</span>{% endif %}</p>
      <p class="home-links">
        {%- if pub.layout == "project" %}
        <a class="home-link" href="{{ pub.url | relative_url }}">Project Page</a>
        {%- endif %}
        {%- if pub.pdf %}
        <a class="home-link" href="{{ pub.pdf }}">arXiv PDF</a>
        {%- endif %}
      </p>
    </div>
  </article>
  {%- endfor %}
</section>

<section class="home-section" id="languages">
  <h2>Languages</h2>
  <div class="home-grid">
    <p><strong>Chinese</strong><br>Native proficiency</p>
    <p><strong>English</strong><br>Professional working proficiency</p>
    <p><strong>German</strong><br>Good working proficiency</p>
  </div>
</section>
