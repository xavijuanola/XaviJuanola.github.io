---
permalink: /
title: "Xavier Juanola Molet"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I received my Bachelor degree in **Physics** at [Universitat de Barcelona (UB)](https://www.ub.edu) in 2018. One year later I got my **Msc in Artificial Intelligence** from [Universitat Pompeu Fabra (UPF)](https://www.upf.edu/) in Barcelona. 

I have been 3 and a half years working in the industry as a Data Scientist, and coursing a **Msc in Astrophysics and Cosmology** as a hobby. Currently doing my **PhD on Sound Localization** at [Image Processing and Computer Vision Group (IPCV)](https://www.upf.edu/web/ipcv), under Prof. [Gloria Haro](https://www.upf.edu/web/gloria-haro)'s supervision. 

I am interested in the artificial intelligence field, more specifically in Deep Learning and computer vision.

<!-- Publications Section -->
## Publications

<ul class="publication-list">
  {% assign sorted_publications = site.publications | sort: 'date' | reverse %}
  {% for post in sorted_publications %}
  <li class="publication-item">
    <div class="publication-image">
      <img src="{% if post.image and post.image != "" %}{{ post.image }}{% else %}/assets/images/publications/blank.png{% endif %}" alt="thumbnail" width="100px" height="100px">
    </div>
    <div class="publication-content">
      <!-- Title as a link to project or arXiv -->
      <h3>
        <a href="{% if post.projecturl and post.projecturl != "" %}{{ post.projecturl }}{% else %}{{ post.arxivurl }}{% endif %}" class="publication-title">
          {{ post.title }}
        </a>
      </h3>
      <p class="authors"><strong>Authors:</strong> 
        {% for author in post.authors %}
          <a href="{{ author.website }}" class="author-link" target="_blank">{{ author.name }}</a>{% unless forloop.last %}, {% endunless %}
        {% endfor %}
      </p>
      <p class="venue"><strong>Venue:</strong> {{ post.venue }}</p>
      <div class="publication-links">
        {% if post.projecturl and post.projecturl != "" %}
        <a href="{{ post.projecturl }}" target="_blank" class="publication-link">
          <img src="/assets/images/icons/globe.png" alt="Project icon" width="16px" height="16px"> Project page
        </a>
        {% endif %}
        
        {% if post.paperurl and post.paperurl != "" %}
        <a href="{{ post.paperurl }}" target="_blank" class="publication-link">
          <img src="/assets/images/icons/pdf.png" alt="PDF icon" width="16px" height="16px"> PDF
        </a>
        {% endif %}
        
        {% if post.arxivurl and post.arxivurl != "" %}
        <a href="{{ post.arxivurl }}" target="_blank" class="publication-link">
          <img src="/assets/images/icons/arxiv.png" alt="arXiv icon" width="16px" height="16px"> arXiv
        </a>
        {% endif %}
        
        {% if post.githuburl and post.githuburl != "" %}
        <a href="{{ post.githuburl }}" target="_blank" class="publication-link">
          <img src="/assets/images/icons/github.png" alt="GitHub icon" width="16px" height="16px"> Code
        </a>
        {% endif %}
      </div>
    </div>
  </li>
  {% endfor %}
</ul>

<style>
  .publication-list {
    list-style: none;
    padding: 0;
  }
  .publication-item {
    display: flex;
    margin-bottom: 15px;
    align-items: center;
  }
  .publication-image {
    margin-right: 20px;
  }
  .publication-content {
    max-width: 80%;
    font-size: 0.85em;
  }
  .authors, .venue {
    margin: 0;
  }
  .publication-links {
    margin-top: 8px;
  }
  
  /* Style for author links to look like normal text but be clickable */
  .author-link {
    color: inherit;
    text-decoration: none;
    cursor: pointer;
  }
  .author-link:hover {
    text-decoration: underline;
  }
  
  /* Style for title to be a link but not underlined */
  .publication-title {
    color: inherit;
    text-decoration: none;
  }
  .publication-title:hover {
    text-decoration: underline;
  }
  
  .publication-link {
    font-size: 0.75em;
    margin-right: 10px;
    display: inline-flex;
    align-items: center;
  }
  .publication-link img {
    margin-right: 5px;
  }
</style>
