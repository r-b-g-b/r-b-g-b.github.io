---
layout: post
title: "Mapping diversity in the Bay Area"
date: 2015-10-21 6:00:02
categories: post projects data geospatial
---

In September 2014, some fascinating work from the [Weldon Cooper Center for Public Service](http://www.coopercenter.org/) made the rounds on the internet. The [Racial Dot Map](http://demographics.coopercenter.org/DotMap/) project accomplished the impressive feat of generating a map of the United States made of of dots. Not just any dots though. Each dot represents (roughly) the residence of a single US citizen, color coded by that person's race. In addition to being lovely to look at, the map reveals some interesting patterns of how people of different races live together (or in some cases, live very far apart from each other).

One thing I really love about the Bay Area is how diverse it is, and I became curious about what these data would show about my community.

The Racial Dot Map makes it very obvious where certain races are concentrated, and to some extent, it points out areas where one or two races predominate. But I wanted to visually explore something slightly different; I wanted visualize diversity *itself*. So instead of splotches of color that represent the presence of individual races, areas would be color coded by how homogeneous or heterogeneous they were. Consider an area containing 100 people. If that area contained 100 white people, it would have the same score as if it had 100 Hispanic people, the lowest possible diversity score. If it had 50 black people and 50 Asian people, it would attain a higher score, but the same as if it had with 50 white people and 50 Asian people. It would attain the highest possible diversity score when it had an even split of all the races recorded by the US census: 20 white people, 20 black people, 20 Asian people, 20 Hispanic people, and 20 "other race" people (an unfortunate category, I know). I analyzed the diversity of census tracts, which contain on average about 4000 people in this sample.

Here are the results: dark regions represent places with high diversity. In broad strokes, the East Bay is most diverse (yeeeeee), followed by SF and North Bay. If you want to delve a bit deeper into the demographics underlying the diversity index in a census tract, you can click on the little dot in the center of the tract to pop up the breakdown. For example, in 2010 my neighborhood had 3716 people, 1256 White, 1163 Black, 750 Hispanic, and 313 Asian and 234 other.

<br>

<a href="/resources/bayarea-diversity-choropleth.html" target="_blank" style="float:right; font-size:80%">view full screen</a>

<iframe src="/resources/bayarea-diversity-choropleth.html" width="100%" height="500px" style="border:none"></iframe>

<br>

Check out <a href="/resources/bayarea-diversity-notebook.html" target="_blank">this Jupyter notebook</a> if you want more detail about how I went about finding, analyzing, and plotting the data.

I'd like to revisit this someday with a smarter measure of diversity. The index I came up with is blind to data outside of an individual census tract. Most people leave their census tracts every once in a while, so capturing larger-scale diversity would make this measure more realistic. For example, even the least diverse places in the Bay Area are probably just a 20 minute drive away from very diverse areas. A better metric would probably include something like, how large of a radius would you have to draw around your census tract to find as many people of non-predominant races as that tract has of its predominant race. For example, if my tract has 1000 Hispanic people, how big of an circle would I have to include around my tract to find 1000 non-Hispanic people? A measure like that, one that includes a concept of distance, would probably go much further towards capturing how diverse a place really feels.