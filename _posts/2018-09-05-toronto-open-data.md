---
layout: post
title: Toronto Open Data Visualizations
---

Back in 2017, I was part of the [Open Toronto meetup](https://www.meetup.com/opentoronto/?_cookie-check=KCWjzTFx54pjoUAa),
and got to mingle with some highly knowledgable data analysis and scientists
alongside government officials and civic-minded Torontonians.  I also made a
few analyses and visualizations of city data.  I've ported a few here to test
if I can embed [plotly HTML figures](https://plot.ly/python/embedding-plotly-graphs-in-HTML/).

If you'd like to know the context for each of these figures, have a look at my
[Open Toronto page](https://cczhu.github.io/OpenDataToronto/), or click on one
of the links below.

# Toronto City Sidewalk Inventory

The [Toronto Sidewalk Inventory](https://www.toronto.ca/services-payments/streets-parking-transportation/walking-in-toronto/toronto-sidewalk-inventory/)
is a geospatial dataset that gives the availability of sidewalks along
Toronto's transportation corridors.  I plot a map of these sidewalks, and
[investigate](https://nbviewer.jupyter.org/github/cczhu/OpenDataToronto/blob/master/SidewalkInventory/Toronto%20Sidewalk%20Inventory%20(Open%20Data%202017-4-20).ipynb)
the correlation between lack of sidewalks along the roads of a
neighbourhood with its population density and median household income.

<div class="container" style="width:100%; background-color:#fff;">
    <img src="{{ site.url }}/img_post/2018-09-05-toronto-open-data/toronto_sidewalks.png">
</div>
&nbsp;
<center>
<i>Plot of sidewalk availability status for the roadways of Toronto, with the
old Toronto municipality boundaries overplotted for reference.  Colours
indicate roadway type and sidewalk availability.  Red, yellow and green roads
indicate no sidewalks, sidewalk available on one side of the road only, and
available on both sides, respectively, while light and blue roads are actually
walkways, pathways or recreational trails.</i>
</center>
&nbsp;

# MyDem0cracy

The [MyDem0cracy](https://mydem0cracy.ca/) Canadian electoral reform survey
(note the replacement of "o" by "0") was produced by a group of concerned
citizens as a complementary survey to the
[controversial](http://www.cbc.ca/news/politics/mydemocracy-survey-results-electoral-reform-1.3950671)
[MyDemocracy.ca](http://news.gc.ca/web/article-en.do?nid=1165179) survey by
the Government of Canada.  The survey solicits freeform comments from
participants, which are then posted to let subsequent participants vote
("agree", "disagree" or "neutral") on the comments.  I
[investigate](https://nbviewer.jupyter.org/github/cczhu/OpenDataToronto/blob/master/MyDem0cracy/MyDemocracy%20(Open%20Toronto%202017-2-23).ipynb)
the consensus opinion arising from these comments, and attempt to determine
clusters of voters with similar opinions.

{% include_relative toronto-open-data/mydem0cracy_stdevvsmean.html %}
&nbsp;
<center>
<i>Plot of vote standard deviation vs. vote arithmetic mean of MyDem0cracy
Canadian electoral reform survey comments. Marker sizes represent the total
number of votes a comment received, while colour represents the response
fraction, the percentage of people who visitied MyDemo0cracy.ca since the
question was posted that voted on the comment.  The dashed grey line represents
the largest standard deviation value for a given mean.  Hover the mouse over a
marker to read the text of its comment and the number of agree, disagree and
neutral votes for it.</i>
</center>
&nbsp;

# Ontario Trillium Fund

The [Ontario Trillium Foundation (OTF)](http://www.otf.ca/) is an agency of the
Ontario provincial government that allocates more than $136 million annually in
social/community program funding annually province-wide.  In accordance with the
Ontario government's Open Data Directive, OTF provides data on grant applications
over the last two decades on their [open data page](http://www.otf.ca/open).  I
[perform](https://nbviewer.jupyter.org/github/cczhu/OpenDataToronto/blob/master/OTF/Ontario%20Trillium%20Foundation%20Grants%20%28Open%20Data%20Toronto%202016-11-24%29.ipynb)
an exploratory analysis on this data, examining how aggregate, per-capita and
per-project funding, and how it is divided into different project areas, have
changed during that time.  I also break down funding for different populations
served, and examine how funding is divided between Ontario's geographic regions.

{% include_relative toronto-open-data/otf_ontario.html %}
&nbsp;
<center>
<i>Per-capita OTF Spending in Ontario's census geographic regions.  Brighter and
more orange colours represent higher funding per capita.  Populations are taken
from 2011 census, and annual funding is averaged from its FY 2010 to 2016 values.
Hover the mouse over a census area to see its name, population, number of OTF
grants given per year, funding per year, median funding per project, and
funding per capita (all OTF values are also averaged from FY 2010 to 2016).</i>
</center>
&nbsp;