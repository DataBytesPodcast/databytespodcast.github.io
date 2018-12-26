---
layout: post
title:  "Episode 5: The Do's and Don'ts of Data Visualization"
date:   2018-12-28
categories: episode
podcast_link: 2h3xaa/episode4_-_12_18_18_6_13_PM.mp3
podcast_file_size: 39.5 MB
podcast_duration: "26:51"
podcast_length: 38667411
podcast_description: "Data visualization is an integral pre-cursor to data analysis, providing a way to visually inspect the data for surprising trends and uncover potential errors in coding. In this episode, we cover some guiding principles of data visualization. Our website contains links to examples."
---

Data visualization is an integral pre-cursor to data analysis, providing a way to visually inspect the data for surprising trends and uncover potential errors in coding. In this episode, we cover some guiding principles of data visualization. A brief summary (including promised links to examples) is included below the player.

<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/547041969&color=%2327a79c&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>

<h4>A summary of do's and don'ts:</h4>
<ul>
<li><b>Do:</b> Label everything, concisely. (This includes specifying the units!)</li>
<li><b>Do:</b> Make sure the plot suits the kind of variable(s). Univariate plots –- histograms or barplots. Bivariate plots -– boxplots, scatterplots, stacked barplots, etc.</li>
<li><b>Do:</b> Report/show plots that tell you something interesting -- and then say why it is interesting in words. Maybe it uncovers an unusual feature of the data, or outliers, or it suggests some kind of underlying associations that warrant further investigation.</li>
<li><b>Do:</b> Carefully choose how many bins to use in your histograms. Or use density plots. (<a href="https://statistics.laerd.com/statistical-guides/understanding-histograms.php">Example of how bin width choice matters</a>)</li>
<li><b>Don't:</b> Use too many colors (see bad pie chart below).</li>
<li><b>Don't:</b> Use smoothing procedures with more flexibility than you can accommodate with the number of observations that you have.
<div class="row">
  <div class="col-sm-8">
  <p><a href="http://htmlpreview.github.io/?https://gist.githubusercontent.com/swang87/fe16a765308c101216f7614cbd4d38b0/raw/2d000ea1c803b7f70fea10a848af10ce83657090/databytes_smoothing.html">Example mentioned</a> in the podcast.</p>
  <p>To the right, we show another example taken from a Fitbit app screenshot (from one of our co-hosts). Note how despite an absence of data points between 2016 and 2018 (shown in the white line) does not prevent the app from interpolating with some parabolic spline in the region (blue curve). The blue curve fabricates an upward trend from 2016 to 2017 and then a downward trend from 2017 to 2018. </p>
  </div>
  <div class="col-sm-4"><img src="/static/img/ep5_fitbit.png" width="200"></div>
</div></li>
<li><b>Do:</b> Jitter scatterplots to minimize overplotting. Or use translucency features of your plotting tool. (<a href="https://python-graph-gallery.com/134-how-to-avoid-overplotting-with-python/">Fixing overplotting in Python</a> | <a href="https://towardsdatascience.com/overshadowing-the-other-points-the-overplotting-issue-e6d1ebbdef20">Fixing overplotting in R</a>)</li>
<li><b>Do: </b>Sort your categorical variables (barplot categories based on heights or boxplot categories based on medians). (<a href="https://moderndive.com/C-appendixC.html">Example</a>)</li>
<li><b>Don't:</b> Use pie charts. More on that below!</li>
</ul>
<hr>
<h3>The Issue with Pie Charts</h3>

<figure>
<img src="https://66.media.tumblr.com/698249f0a55f9186d52d252759242532/tumblr_p3utcdJEdu1sgh0voo1_1280.jpg">
<figcaption>
Source: <a href="http://viz.wtf/image/171134950336">WTF Visualizations</a>.
</figcaption>
  </figure>
<br>
This image just about encapsulates everything that is wrong with pie charts.
<ul>
<li>There are too many categories, making it difficult to discern which category is associated with which slice.</li>
<li>The angling of the pie makes it hard to visually process the relative sizes of each slice.</li>
<li>The pie chart occupies a lot of space for the information it is trying to convey.</li>
</ul> 
<p>You can find multiple posts online that expand on why pie charts are often bad ways of visualizing data -- yes, there are longer rants on pie charts than the one we've given, such as the one <a href="https://www.businessinsider.com/pie-charts-are-the-worst-2013-6"> here</a>. We particularly like an example of why even simple pie charts (with few categories displayed) can fail:</p>
<img src="https://amp.businessinsider.com/images/51bf1e9becad048c0a000002-960-326.jpg" width="500"><br>
<p>The example provided suggests that A, B, and C are pie charts that represent polling results for a 5-candidate race in a local election, done at 3 different time points. Can you tell who's in the lead at each time point?  </p>
<img src="https://amp.businessinsider.com/images/51bf0aa8ecad04a05d00004a-960-369.jpg" width="500"><br>
<p>The bar charts here represent the same data. Not only can you tell who's in the lead at any of the 3 time points, but you can also easily tell the trajectory of how each candidate fared as time progressed. </p>
<p>This leads us to our favorite pie chart:</p>
<figure><img src="https://i.imgur.com/aRLRqwj.png"><figcaption>
  Source: <a href="https://imgur.com/gallery/aRLRqwj">imgur</a>.
</figcaption></figure>
<h3>The Naughty List</h3>
Now we present a list of some other truly horrific charts (that are not pie charts).
<ol><li>
  <figure>
  <img src="http://livingqlikview.com/wp-content/uploads/2017/04/Worst-Data-Visualizations-05.jpg">
    <figcaption>
      Source: <a href="http://livingqlikview.com/the-9-worst-data-visualizations-ever-created/">The 9 Worst Data Visualizations Ever Created</a>
    </figcaption>
  </figure>
  <p>Pie charts aren't the only culprits. Here, the y-axis scale is deceiving.</p>
</li>
<li>
<div class="row">
  <div class="col-sm-4"><figure><img src="https://junkcharts.typepad.com/.a/6a00d8341e992c53ef01b8d2464d49970c-200wi">
<figcaption>Source: <a href="https://junkcharts.typepad.com/junk_charts/wsj/">Junk Charts</a></figcaption>
</figure></div>
  <div class="col-sm-8"><p>This plot, cut out of the Wall Street Journal, requires prolonged staring to realize how the bar lengths might possibly reflect any of the proportions provided. There's conditioning involved, in which case, a mosaicplot will probably do the data better justice, as suggested at the source website.</p>
</div>
</div>


</li>
<li>
<figure><img src="https://visme.co/blog/wp-content/uploads/2016/02/Percent-of-Job-Loses-Relative-to-Peak-Employment-Month.jpg" width="700">
<figcaption>Source: <a href="https://visme.co/blog/bad-infographics/">Bad Infographics: 11 Mistakes You Never Want to Make</a></figcaption></figure>
<p>Too many colors can make it challenging to differentiate various categories.</p>
</li>
</ol>
<h3>The Nice List</h3>
Finally, this discussion wouldn't be complete with some stellar examples of thoughtful graphics.
<ol>
<li><figure><img src="https://raw.githubusercontent.com/halhen/viz-pub/master/pastime-income/pastime.png" width="500"><figcaption>Source: <a href="https://www.reddit.com/r/dataisbeautiful/comments/6heb75/income_distributions_in_americans_pastimes_oc/">Reddit post</a></figcaption></figure>
<p>This plot showcases how American pastimes differ by household income, using the American Time Use Survey dataset.</p></li>
<li><figure><img src="https://fivethirtyeight.com/wp-content/uploads/2016/11/morris-durant-1b.png?w=575">
<figcaption>Source: <a href="https://fivethirtyeight.com/features/the-52-best-and-weirdest-charts-we-made-in-2016/">Fivethirtyeight.com</a></figcaption></figure>
<p>Ah, a plot of residuals (points per shot against expectations) to showcase the superiority of basketball players. Minor quibble: Not too sure why Curry, Thompson, Barnes, and Green have the same colors whereas other highlighted players are in different colors.</p>
</li>
<li><figure><img src="/static/img/ep5_gapminder.png">
<figcaption>Source: <a href="https://s3-eu-west-1.amazonaws.com/static.gapminder.org/GapminderMedia/wp-uploads/20161215212516/countries_health_wealth_2016_v151.pdf">Gapminder</a>
</figcaption></figure><p>Indeed, this example, from the late great Hans Rosling's organization, Gapminder, is an example of where arguably a lot of information is fit into a small space. However, this is one of those plots that is actually meant to encourage zooming in and taking a good look (the source link above will lead you to the full pdf image). Even in this shrunken view, the color-coding by region helps provide a big-picture look at the relationship between health and wealth of nations around the world. The sizes of the circles additionally showcase the population size of each nation.</p></li>
</ol>
 <h3>Looking for more?</h3>
 There's a whole <a href="reddit.com/r/dataisbeautiful/">subreddit</a> (/r/dataisbeautiful) full of them. We use these sometimes as inspiration -- but of course, because Reddit is a free-for-all platform, not every post will be golden.
