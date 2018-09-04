---
title: Contact
homepage: true
id: contact
---

Please feel free to reach out to me!

<div id="contactbuttons" class="container">
<div class="row">
<div class="col-sm-8 col-sm-offset-2">
  <div class="row">
  {% for link in site.social-network-links %}
    {% assign curkey = link[0] %}
    {% assign element = site.data.SocialNetworks[curkey] %}
    <div class="col-xs-4 contact-item">
    {% if curkey == 'rss' %}
      <a href="{{ '/feed.xml' | prepend: site.baseurl }}" title="{{ element.name }}">
    {% else %}
      <a href="{{element.baseURL}}{{ site.social-network-links[curkey] }}" title="{{ element.name }}">
    {% endif %}
        <span class="fa-stack fa-lg" aria-hidden="true">
          <i class="fa fa-circle fa-stack-2x"></i>
          <i class="fa {{ element.icon }} fa-stack-1x fa-inverse"></i>
        </span>
        <span class="sr-only">{{ element.name }}</span>
      </a>
    </div>
  {% endfor %}
  </div>
</div>
</div>
</div>

<!-- <div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1" style="width:100% padding-top=100px">
<ul class="list-inline text-center social-links">
  {% for link in site.social-network-links %}
    {% assign curkey = link[0] %}
    {% assign element = site.data.SocialNetworks[curkey] %}
    <li>
    {% if curkey == 'rss' %}
      <a href="{{ '/feed.xml' | prepend: site.baseurl }}" title="{{ element.name }}">
    {% else %}
      <a href="{{element.baseURL}}{{ site.social-network-links[curkey] }}" title="{{ element.name }}">
    {% endif %}
        <span class="fa-stack fa-lg" aria-hidden="true">
          <i class="fa fa-circle fa-stack-2x"></i>
          <i class="fa {{ element.icon }} fa-stack-1x fa-inverse"></i>
        </span>
        <span class="sr-only">{{ element.name }}</span>
      </a>
    </li>
  {% endfor %}
</ul>
<p class="copyright text-muted"> -->

<!--         <div class="col-md-4 portfolio-item">
            <a href="{{ cproj.url }}" class="portfolio-link" data-toggle="modal">
                <div class="portfolio-img-container">
                <img src="{{ cproj.img }}" class="portfolio-img img-responsive img-centered" alt="">
                  <div class="overlay"></div>
                </div>
            </a>
            <div class="portfolio-caption">
                <h3>{{ cproj.name }}</h3>
                <p class="text-muted">{{ cproj.desc }}</p>
            </div>
        </div> -->
