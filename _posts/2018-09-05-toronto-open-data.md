---
layout: post
title: Toronto Open Data Visualizations
---

Back in 2017, I was part of the [Open Toronto meetup](https://www.meetup.com/opentoronto/?_cookie-check=KCWjzTFx54pjoUAa),
and got to mingle with some highly knowledgable data analysis and scientists
alongside government officials and civic-minded Torontonians, while making a
few of my own analyses and visualizations of city data.  I've created a small
showcase of visualizations here (partly to see if I can embed [plotly HTML
figures](https://plot.ly/python/embedding-plotly-graphs-in-HTML/)).

If you'd like to know the context for each of these figures, please have a look
at my [Open Toronto page](https://cczhu.github.io/OpenDataToronto/), or click
on one of the links below.

# Toronto City Sidewalk Inventory

The [Toronto Sidewalk Inventory](https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#3763d352-5f0a-4385-4cec-f255d4860ea5)
is a geospatial dataset that gives the availability of sidewalks along
Toronto's transportation corridors.  I plot a map of these sidewalks, and
investigate the correlation between lack of sidewalks along the roads of a
neighbourhood with its population density and median household income.  I find
that the fraction of underdeveloped or missing sidewalk tends to depend on
population density and on zoning, with densely populated areas and residential
and commercial zones having very little missing sidewalk.  Missing sidewalk,
however, is not correlated with neighbourhood income, so there doesn't appear
to be any favouritism from city hall toward richer neighbourhoods.

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
citizens as a complementary survey to the [controversial](http://www.cbc.ca/
news/politics/mydemocracy-survey-results-electoral-reform-1.3950671)
[MyDemocracy.ca](https://www.canada.ca/en/campaign/electoral-reform/participate-in-canadian-federal-electoral-reform-consultations/mydemocracyca.html)
survey by the Government of Canada.  The survey solicits freeform comments
from participants, which are then posted to let subsequent participants vote
("agree", "disagree" or "neutral") on the comments.  I investigate the
consensus opinion arising from these comments, and attempt to determine
clusters of voters with similar opinions.  In the aggregate, I find that
particiapnts are all highly in favour of greater political education and civic
engagement.  They disagree, however, with how electoral reform should proceed,
with one large group of users advocating for proportional representation,
another in favour of the current system, and a third without a strong opinion
either way.

{% include_relative toronto-open-data/mydem0cracy_stdevvsmean.html %}
&nbsp;
<center>
<i>Plot of vote standard deviation vs. vote arithmetic mean of MyDem0cracy
Canadian electoral reform survey comments. Marker sizes represent the total
number of votes a comment received, while colour represents the response
fraction, the percentage of the people who visitied MyDemo0cracy.ca since the
question was posted that voted on the comment.  The dashed grey line
represents the largest standard deviation value for a given mean.  Hover the
mouse over a marker to read the text of its comment and the number of agree,
disagree and neutral votes for it.</i>
</center>
&nbsp;

# Ontario Trillium Fund

The [Ontario Trillium Foundation (OTF)](http://www.otf.ca/) is an agency of the
Ontario government that annually allocates more than $136 million dollars in
social/community program funding province-wide.  In accordance with the Ontario
government's Open Data Directive, OTF provides data on successful grant
applications over the last two decades on their [open datapage](http://www.otf.ca/open).
I perform an exploratory analysis on this data, examining how aggregate,
per-capita and per-project funding is divided into different project areas and
geographic regions, and how this changes with time. I find that:

* The total amount of OTF annual funding per capita has gone down by about 20%
over the last two decades.
* The total number of grants has gone down by a factor of 2 since 2011, most
pronounced in the number of arts and sports & recreation grants.  The amount
per grant has gone up by about 50%.
* While geographic regions with larger populations typically get more money in
total, they get around 30% *less* money per capita.  This is likely because
urban areas are wealthier and already have established resources and
institutions, and so need funding less.

{% include_relative toronto-open-data/otf_ontario.html %}
&nbsp;
<center>
<i>Per-capita OTF Spending in Ontario's census geographic regions.  Brighter and
warmer colours represent higher funding per capita.  Populations are taken
from 2011 census, and annual funding is averaged from its FY 2010 to 2016 values.
Hover the mouse over a census area to see its name, population, number of OTF
grants given per year, funding per year, median funding per project, and
funding per capita (all OTF values are also averaged from FY 2010 to 2016).</i>
</center>
&nbsp;