## Bayesian Statistics 

Bayesian statistics is a particular approach to applying probability to statistical problems. It provides us with mathematical tools to update our beliefs about random events in light of seeing new data or evidence about those events.

**Bayesian x Frequentist statistics**
* Bayesian statistics provides us with mathematical tools to rationally update our subjective beliefs in light of new data or evidence.
* The frequentist definition of probability is based on observation of a large number of trials. On the other hand, the Bayesian definition of probability P(E) reflects our prior beliefs, so P(E) can be any probability distribution, provided that it is consistent with all of our beliefs. 
* Frequentist statistics tries to eliminate uncertainty by providing estimates. Bayesian statistics tries to preserve and refine uncertainty by adjusting individual beliefs in light of new evidence.
* *Bayesian probability represents uncertainty while frequentist probability represents relative frequency.* 
* The two definitions result in different methods of inference. Using the frequentist approach, we describe the confidence level as the proportion of random samples from the same population that produced confidence intervals which contain the true population parameter.

EXAMPLE: 
*If we generated 100 random samples from the population, and 95 of the samples contain the true parameter, then the confidence level is 95%. Note that each sample either contains the true parameter or does not, so the confidence level is NOT the probability that a given interval includes the true population parameter.*

*The correct interpretation is: 95% of random samples of 1,500 adults will produce confidence intervals that contain the true proportion of Americans who think the federal government does not do enough for middle class people.*

*Here are two common misconceptions:*

    * *There is a 95% chance that this confidence interval includes the true population proportion*.

    * *The true population proportion is in this interval 95% of the time*.

*The probability that a given confidence interval captures the true parameter is either zero or one. To a frequentist, **the problem is that one never knows whether a specific interval contains the true value with probability zero or one. So a frequentist says that “95% of similarly constructed intervals contain the true value**”.*

*The second (incorrect) statement sounds like the true proportion is a value that moves around that is sometimes in the given interval and sometimes not in it. Actually the true proportion is constant, it’s the various intervals constructed based on new samples that are different.*

*The Bayesian alternative is the credible interval, which has a definition that is easier to interpret. Since a Bayesian is allowed to express uncertainty in terms of probability, a Bayesian credible interval is a range for which the Bayesian thinks that the probability of including the true value is, say, 0.95. Thus a Bayesian can say that there is a 95% chance that the credible interval contains the true parameter value.*

### Conditional Probability 
![image](https://user-images.githubusercontent.com/39881974/208296189-79befa10-a18d-4689-9328-b625303b250a.png)

Which is read as "the probability of event A occurring, given event B occurs". An important thing to remember is that conditional probabilities are not the same as their inverses.That is, the "probability of event A given event B" is not the same thing as the "probability of event B, given event A".

### Bayes Rule
![image](https://user-images.githubusercontent.com/39881974/208296088-7f14c040-62f6-4fc1-8567-4a1a73d37929.png)

* **Posterior probability** (updated probability after the evidence is considered)
* **Prior probability** (the probability before the evidence is considered)
* **Likelihood** (probability of the evidence, given the belief is true)
* **Marginal probability** (probability of the evidence, under any circumstance)

Bayes' Rule tells you how to calculate a conditional probability with information you already have. It is helpful to think in terms of two events – a hypothesis (which can be true or false) and evidence (which can be present or absent).
However, it can be applied to any type of events, with any number of discrete or continuous outcomes.

![image](https://user-images.githubusercontent.com/39881974/208296264-2dcec515-b1ff-4a8f-a42b-0d5cec751477.png)

Bayes' Rule lets you calculate the posterior (or "updated") probability. This is a conditional probability. It is the probability of the hypothesis being true, if the evidence is present.

Think of the prior (or "previous") probability as your belief in the hypothesis before seeing the new evidence. If you had a strong belief in the hypothesis already, the prior probability will be large.

The prior is multiplied by a fraction. Think of this as the "strength" of the evidence. The posterior probability is greater when the top part (numerator) is big, and the bottom part (denominator) is small.

The numerator is the likelihood. This is another conditional probability. It is the probability of the evidence being present, given the hypothesis is true.

Now look at the denominator. This is the marginal probability of the evidence. That is, it is the probability of the evidence being present, whether the hypothesis is true or false. The smaller the denominator, the more "convincing" the evidence.

### Bayes Updating 
* Process of using Bayes rule to update a probability based on an event affecting it. 
* More generally, the what one tries to update can be considered ‘prior’ information, sometimes simply called the prior. The event providing information about this can also be data. Then, updating this prior using Bayes’ rule gives the information conditional on the data, also known as the posterior, as in the information after having seen the data. Going from the prior to the posterior is Bayes updating.

Given some data D which contains the one d_1 data point, then our posterior is:

![image](https://user-images.githubusercontent.com/39881974/208701767-41ee5aab-ba3b-442a-86fe-0e87dc24a7ed.png)

Lets say we now acquire another data point d_2, so we have more evidence to evaluate and update our belief (posterior) on. However, our prior now becomes our old posterior because this represents our new prior belief of our hypothesis:

![image](https://user-images.githubusercontent.com/39881974/208701938-29c9be57-fe6a-4be0-b34f-92664ec20e14.png)

In terms of updating, we say that the posterior is proportional to the product of the likelihood and prior:

![image](https://user-images.githubusercontent.com/39881974/208702128-bc6bb3ec-7207-4ad0-ba69-a50db996ccad.png)




