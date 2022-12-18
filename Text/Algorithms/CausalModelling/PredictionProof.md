## Prediction and Proof 


### Explain x Predict

![image](https://user-images.githubusercontent.com/39881974/208303846-0baee543-4171-4f7b-9b15-55fc0be122ff.png)

 One group is focused on good explanatory power and assumes that if I have a model that explains well, it will predict well too. 
 They are applying statistical ideas, but in areas like the social sciences, business, and industry. 
 Another group is focused on predictive power, and assumes that if you have good prediction, 
 then the model must also have good explanatory power. 
 Both of these assumptions are dangerous by the way. The second group is, of course, more your data mining and machine learning crowd. 
 Statisticians end up being the third group. She explains this in one of the keynotes. They're more like the explain group, but frankly, 
 the explain group doesn't always analyze data quite the way that a statistician might, or might approve of. For instance, 
 the explain group tends to try to prove cause with regression. I think what is most likely occurring is that not everybody's 
 familiar with causal modeling. So, some researchers do the best job they can with the tools they have. She then goes on to explain 
 five key differences. For the explain group, theory is king, hypotheses, much like David Cox was describing in response to Breiman. 
 For the predictive group, data is king. For the explain group, their goal is to explain causation. Now again, they may not be using 
 causal models, but that's what they're attempting to do. They're attempting to explain causation. For the predict group, often 
 correlation or mere association is sufficient. If you are trying to figure out what someone is going to watch next on Netflix, you 
 might not need a causal model. Correlation might be enough. For the explain group, they tend to be retrospective. The predict group 
 has to be prospective. If not, they're not doing the job. They're trying to make future micro decisions. The explain group is mostly 
 focused on bias. You may be familiar with the bias variance trade off. That's what she's referring to here. Bias is accuracy. 
 For the explain group, that's the focus, the accuracy, but for the predict group, bias isn't enough. They also have to worry about 
 variance because variance gives you an idea of how well your data will generalize to future situations, and if you're predicting, 
 that's really important. The next one I think is really key. The explain group is focused on the average case. What's 
 happening overall? Where is that regression line? Where is that trend line? The predict group is focused on the individual case. 
 The risk score, the propensity score, is this individual insurance claim likely showing signs of fraud. I think the reason that her 
 research and speaking is so powerful is that as this list makes clear, you can't optimize for both at the same time. 
 You will make different choices during model development and model selection based on these priorities. So, and this is the key point. 
 If you are focused on explain, you won't get good prediction as some kind of a bonus, and if you are focused on prediction, you won't 
 get good explanation as a bonus. Now, again, we don't mean something like explainable AI. We mean explanation the way the explain folks
 would describe it or want to perform it. So you have to be clear on your objectives, 
 and you must have good communication with your colleagues and your management to ensure that your priorities are consistent with theirs.
