## Bayesian Statistics 

Bayesian statistics is a particular approach to applying probability to statistical problems. It provides us with mathematical tools to update our beliefs about random events in light of seeing new data or evidence about those events.

**Bayesian x Frequentist statistics**
Bayesian statistics provides us with mathematical tools to rationally update our subjective beliefs in light of new data or evidence.
Frequentist statistics assumes that probabilities are the long-run frequency of random events in repeated trials.
Frequentist statistics tries to eliminate uncertainty by providing estimates. Bayesian statistics tries to preserve and refine uncertainty by adjusting individual beliefs in light of new evidence.

Bayesian probability represents uncertainty while frequentist probability represents relative frequency. 

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

