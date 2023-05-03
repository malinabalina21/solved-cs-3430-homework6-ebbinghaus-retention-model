Download Link: https://assignmentchef.com/product/solved-cs-3430-homework6-ebbinghaus-retention-model
<br>
After taking a class students rarely retain all the material covered in that class. Some retain more, some – less. Let <em>r</em>(<em>t</em>) be the percentage of the material that the student can recall <em>t </em>weeks later. The psychologist Hermann Ebbinghaus (<a href="https://en.wikipedia.org/wiki/Hermann_Ebbinghaus">https:</a>

<a href="https://en.wikipedia.org/wiki/Hermann_Ebbinghaus">//en.wikipedia.org/wiki/Hermann_Ebbinghaus</a><a href="https://en.wikipedia.org/wiki/Hermann_Ebbinghaus">)</a> found that this percentage of retention can be modeled as <em>r</em>(<em>t</em>) = (100 − <em>a</em>)<em>e</em><sup>−<em>λt </em></sup>+ <em>a</em>, where <em>λ </em>and <em>a </em>are student specific and such that <em>λ </em>is a positive constant, typically 0 <em>&lt; λ &lt; </em>1, and 0 <em>&lt; a &lt; </em>100.

Write the function percent_retention_model(lmbda, a) that takes two constants lmbda and a and returns a function representation of the Ebbinghaus retention model.

Use your implementation of percent_retention_model(lmbda, a) to implement the function plot_retention(lmbda, a, tl, tu) that takes four constants such that the first two, lmbda and a, are the same as in percent_retention_model,

Figure 1: Ebbinghaus Model of Forgetting.

and the last two, tl and tu, are the lower and upper bound of the x-axis interval on which the plots of the model returned by percent_retention_model and its derivative are plotted. The title of the plot should be ”Ebbinghaus Model of Forgetting,” the x-axis label should be ”t,” and the y-axis label should be ”prf and dprf,” which stand for ”percent retention function” and ”derivative of percent retention function,” respectively. The prf curve should be plotted red, the dprf curve – blue.

Figure 1 is the plot generated with the following call in the Python shell.

&gt;&gt;&gt; plot_retention(make_const(0.5), make_const(15.0), make_const(0.0), make_const(30))

Figure 2 is the plot generated with the following call in the Python shell.

&gt;&gt;&gt; plot_retention(make_const(0.25), make_const(25.0), make_const(0.0), make_const(30))

Let’s find out how much material a student whose <em>λ </em>= 0<em>.</em>5 and <em>a </em>= 15 will retain after 2 weeks.

Figure 2: Ebbinghaus Model of Forgetting. &gt;&gt;&gt; prm = percent_retention_model(make_const(0.5), make_const(15.0))

&gt;&gt;&gt; prmf = tof(prm)

&gt;&gt;&gt; prmf(2)

46.2697524996

Save your code in hw06_s19.py.

<h1>Problem 2: Spread of Diseases</h1>

Suppose the department of public health in the city of X is monitoring the spread of a contagious disease (e.g., a strain of flu). Let X’s population be <em>P</em>. At week <em>t</em><sub>0 </sub>the deparment records that <em>p</em><sub>0 </sub>cases have been reported. At week <em>t</em><sub>1</sub>, such that <em>t</em><sub>0 </sub><em>&lt; t</em><sub>1</sub>, the department records that <em>p</em><sub>1 </sub>cases have been reported.

Write the function spread_of_disease_model(p, t0, p0, t1, p1) that takes five constants where the first constant is the size of the population of X and the other four constants are the values of <em>t</em><sub>0</sub>, <em>p</em><sub>0</sub>, <em>t</em><sub>1</sub>, and <em>p</em><sub>1</sub>, as described in the previous paragraph. This function returns a function representation of the spread model for the disease determined by the given parameters.

Use your implementation of spread_of_disease_model to implement the function plot_spread_of_disease(p, t0, p0, t1, p1, tl, tu) whose first four parameters are the same as the parameters of spread_of_disease_model and the last two, tl and tu, are the lower and upper bound of the x-axis interval on which the plots of the model returned by spread_of_disease_model and its derivative are plotted. The title of the plot should be ”Spread of Disease,” the x-axis label should be ”t,” and the y-axis label should be ”sdf and dsdf,” which stand for ”spread of disease function” and ”derivative of spread of disease function,” respectively. The sdf curve should be plotted red, the dsdf curve – blue.

Figure 3 is the plot generated with the following call in the Python shell.

&gt;&gt;&gt; plot_spread_of_disease(make_const(500000), make_const(0.0), make_const(200.0), make_const(1.0), make_const(500.0), make_const(0.0), make_const(7.0))

Save your code in hw06_s19.py.

Figure 3: Spread of Disease.

<h1>Problem 3: Plant Growth</h1>

Suppose a botanist monitors the growth of a plant X. The botanist records that at day <em>t</em><sub>0 </sub>the plant’s height is <em>h</em><sub>0 </sub>cm and at day <em>t</em><sub>1</sub>, such that <em>t</em><sub>0 </sub><em>&lt; t</em><sub>1</sub>, the plant’s height is <em>h</em><sub>1 </sub>cm. Over time, after watching many plants X grow and recording their growth stages, the botanist observes that at maturity a typical plant X reaches the height of <em>m </em>cm.

Write the function plant_growth_model(m, t0, h0, t1, h1) that takes five constants where the first constant is the height of a typical plant X at maturity and the other four constants are the values of <em>t</em><sub>0</sub>, <em>h</em><sub>0</sub>, <em>t</em><sub>1</sub>, and <em>h</em><sub>1</sub>, as described in the previous paragraph. This function returns a function representation of the plant growth model for a typical plant X determined by the given parameters.

Use your implementation of plant_growth_model to implement the function plot_plant_growth(m, t0, h0, t1, h1, tl, tu) whose first five parameters are the same as the parameters of plant_growth_model and the last two, tl and tu, are the lower and upper bound of the x-axis interval on which the plots of the model returned by plant_growth_model and its derivative are plotted. The title of the plot should be ”Plant Growth,” the x-axis label should be ”t,” and the y-axis label should be ”pgf and dpgf,” which stand for ”plant growth function” and ”derivative of plant growth function,” respectively. The pgf curve should be plotted red, the dpgf curve – blue.

Figure 4 is the plot generated with the following call in the Python shell.

&gt;&gt;&gt; plot_plant_growth(make_const(55.0),

make_const(9.0), make_const(8.0), make_const(25.0), make_const(48.0), make_const(9.0), make_const(50.0))

Save your code in hw06_s19.py.

<h1>Problem 4: Spread of News</h1>

A news item is broadcast by a mass media outlet to a potential audience of <em>P </em>people.

Write the function spread_of_news_model(p, k) that takes two constants that characterize the spread of news among a given population, as we discussed in class, and returns a function representation of the spread of news model determined by these parameters.

Use your implementation of spread_of_news_model to implement the function plot_spread_of_news(p, k, tl, tu) whose first two parameters are the

Figure 4: Plant Growth.

Figure 5: Spread of News.

same as the parameters of spread_of_news_model and the last two, tl and tu, are the lower and upper bound of the x-axis interval on which the plots of the model returned by spread_of_news_model and its derivative are plotted. The title of the plot should be ”Spread of News,” the x-axis label should be ”t,” (time in days) and the y-axis label should be ”snf and dsnf,” which stand for ”spread of news function” and ”derivative of spread of news function,” respectively. The snf curve should be plotted red, the dsnf curve – blue.

Figure 5 is the plot generated with the following call in the Python shell.

&gt;&gt;&gt; plot_spread_of_news(make_const(50000),

make_const(0.3), make_const(0.0), make_const(50.0))

Let’s find out at what rate the news is spreading initially.

&gt;&gt;&gt; sn = spread_of_news_model(make_const(50000),

make_const(0.3))

&gt;&gt;&gt; dsn = deriv(sn)

&gt;&gt;&gt; dsnf = tof(dsn)

&gt;&gt;&gt; dsnf(0)

15000.0

So, initially the rate of outreach is 15,000 people per day. What happens at day 10?

&gt;&gt;&gt; sn = spread_of_news_model(make_const(50000),

make_const(0.3))

&gt;&gt; dsn = deriv(sn)

&gt;&gt;&gt; dsnf = tof(dsn)

&gt;&gt;&gt; dsnf(10)

746.806025518

The rate of outreach drops to 747 people. How about day 30?

&gt;&gt;&gt; sn = spread_of_news_model(make_const(50000),

make_const(0.3))

&gt;&gt; dsn = deriv(sn)

&gt;&gt;&gt; dsnf = tof(dsn)

&gt;&gt;&gt; dsnf(30)

1.8511470613

The rate of outreach is less than 2 people per day. The media outlet had better look for new topics.

A side note for CS seniors and grad students in this class. If you are looking for a project, here is something to think about. Suppose that you take a bunch of corporate media clips, similar to the news collage we watched in lecture 11

(here is the link <a href="https://www.youtube.com/watch?v=qjUvfZj-Fm0">https://www.youtube.com/watch?v=qjUvfZj-Fm0</a> in case you didn’t attend), push each of them through an ASR engine to obtain its transcript, and then model the distribution of corporate cliches such as ”bombshell,” ”walls are closing in,” ”tipping point,” ”beginning of the end,” etc. Once you have reliable cliche distribution models, you can use them to classify news clips as ”character assassination,” ”fear mongering to obtain funding,” etc.

Save your code in hw06_s19.py.