---
title: Projects
homepage: true
id: projects
pagecolor: "#2a283d"
---

For a full list of my publications, please see
[my ArXiv page](https://arxiv.org/a/zhu_c_2.html).

<!-- based off of the portfolio section in Agency
https://github.com/y7kim/agency-jekyll-theme/blob/gh-pages/_includes/portfolio_grid.html -->

<div id="portfolio" class="container">
  <div class="row">
    {% for project in site.projects %}
        {% assign curkey = project[1] %}
        {% assign cproj = site.data.Projects[curkey] %}
        <div class="col-md-4 portfolio-item">
            <a href="{{ cproj.url }}" class="portfolio-link" data-toggle="modal">
                <div class="portfolio-img-container">
                <img src="{{ cproj.img }}" class="portfolio-img img-responsive img-centered" alt="">
<!--                   <div class="overlay"></div> -->
                </div>
            </a>
            <div class="portfolio-caption">
                <h3>{{ cproj.name }}</h3>
                <p>{{ cproj.desc }}</p>
            </div>
        </div>
    {% endfor %}
  </div>
</div>
