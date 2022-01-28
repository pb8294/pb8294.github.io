---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Uncertainty Quantification: An Overview"
summary: "Uncertainty are an inevitable part of a both real life events and computer simulation / modeling and their quantification is a very important and interesting research area."
tags: 
- Uncertainty Quantification
categories: []
date: 2019-11-03T09:44:03-05:00

---

<h2>Overview</h2>
Uncertainty are an inevitable part of a both real life events and computer simulation / modeling and their quantification is a very important and interesting research area. Say you own an industry that manufactures car bumpers and your test requires you to run and crash two cars head on. Considering the two cars have the same speed every time we can bet a million dollars that the cars, individually as well as separately, will never have exact same damages in exact same locations in all the experiments. These are contributed to the fact that there are small variations to the offset between the line of sight of the trajectory, offset in the starting point, the time difference (however small) between the acceleration of the two cars, the difference in direction and many more. We will not be able to give an exact spot of the damage and the extent of the damage and will have to resort to probabilistic way of representing them.

<h2>What introduces these uncertainties?</h2>
There are several factors that cause uncertainties, some of them are:

<b>Model bias</b><br>
This refers to how well a model is represented by a mathematical equation that forms the basis for computer generated models and simulations. Say you are in a thunder prone area and you are in constant fear of getting struck by lightning. You want to model how far away did the lightning strike based on the time you saw the white flash to when you heard the sound. You can multiply the speed of sound and the time to get an estimate of the distance. However, there are variables as the decay of sound due to air resistance, absorption by various structures around and so on which should also be included to make a model complete. Uncertainty arises due to approximations to avoid these factors.

<b>Parameter uncertainty</b><br>
Each model’s output is based on certain weights that are multiplied to the inputs to get the output. The parameters may not be exactly the same each time and in some cases, they might not be known as well. 

<b>Observation uncertainty</b></br>
This is very common in any experiment. In any repeated experiment, say calculating resistance in Ohm’s law by:<br>
	
	Resistance = Voltage / Current

every observer will always read different readings for the same set of experiment.


<b>Numerical uncertainty</b><br>
In solving a complex expression (computer model experiments), there are several approximations made to simplify the experiment. For example, we usually sample a continuous function and approximate its mean as a weighted sum rather than performing integration. These introduce some numerical error that results in uncertainty.

<h2>Introduction to Aleatoric and epistemic uncertainty</h2>
<b>Aleatoric uncertainty:</b><br>
In observation uncertainty, we discussed above, we discussed that in a repeated experiment, the observations are never the same despite keeping track of multiple variables. This statistical uncertainty in the observation in an experiment is what defines Aleatoric uncertainty. We can take an example of linear regression where,

	y = f(x) + error = w.T * x + error

Assume that the output for an input is exact every time i.e. it’s value is focused around f(x) and the variation is defined by the variability of the weights and the error itself. If we say that the output is modelled as a Gaussian distribution then we can either say that:
y ~ N(y | f(x), variance(w, error)) i.e each output has different variance as a function of weights and error with the error added to each observation belonging to different distribution. This is heteroscedastic aleatoric uncertainty
y ~ N(y | f(x), variance) i.e. variance is constant for each observation. This is homoscedastic aleatoric uncertainty

<b>Epistemic uncertainty:</b><br>
These are uncertainty that arises because a measurement may not be accurate. As stated in numerical uncertainty above, this may be due to avoiding certain factors as air resistance to simplify the model. 


<h2>Uncertainty Quantification (UQ) problem:</h2>
<b>Forward UQ:</b><br>
Forward UQ refer to quantifying the uncertainty at the output of the model due to any or all sources of uncertainties from the input, parameters, model, algorithm and others. We obtain a probability distribution of the output instead of a point estimate and provide a mean (most likely value) and variance.

<b>Inverse UQ:</b><br>
Inverser UQ starts with certain observations (x, y) pair observed from field. We run the experiment on the model using the same input and get an output y’. We try to estimate the parameters, model bias term or both that can explain the current discrepancy between the simulated output and the observation.

<b>References:</b><br>
https://en.wikipedia.org/wiki/Uncertainty_quantification
http://www.cs.ox.ac.uk/people/yarin.gal/website/blog_2248.html
https://towardsdatascience.com/what-uncertainties-tell-you-in-bayesian-neural-networks-6fbd5f85648e