---
title: "Data Science Interview Questions with Answers"
datePublished: Fri Oct 09 2020 02:04:03 GMT+0000 (Coordinated Universal Time)
cuid: cl9y3g5dk003e9fnv5y701ug6
slug: data-science-interview-questions-with-answers-f77d78f8ab4f
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1667300126110/fO85DKYOK.png

---

#### A set of most basic and important Data Science Interview Questions to prepare to get the job!

*Support my writing*

**Join Medium.com as a member** through the link below.

[**https://thomascherickal.medium.com/membership**](https://thomascherickal.medium.com/membership)

### The Best Way to Prepare for Interview Questions

Now suppose you read a question about a topic like overfitting. You can read the text and memorize the answer. Usually, articles with this heading (Interview Questions and Answers) are normally constructed that way, with plain text questions and answers. You could follow that route for interview preparation, but it is simply **not the right thing to do.** I can give you a list of important questions, with answers. Which is exactly what I will do in this article, later.

But you need to understand one thing clearly.

**You cannot learn programming and data science from books alone.**

You can learn the heading and the words. **But the concept will truly be understood only in a practical manner; in a mini-project or in a worked-out example on the computer.**

Data science is similar to programming in this regard.

Books are meant to just start your journey.

**The real learning begins only when you implement it in code by yourself.**

**To take an example:**

**Question from the Interviewer:**

**“What is cross-validation and why is it important? How does it eliminate overfitting?”**

**A Good Answer:**

“Cross-validation eliminates overfitting by exposing the model to the entire data set in a statistically uniform manner. Overfitting happens when the training set and test sets are not properly selected. If a model like **LogisticRegression** is trained until the error rate is very small, it may not be able to generalize to the pattern of data found in the test set. Hence the performance of the model would be excellent on the training set, but poor on the test set. **This is because the model has overfitted itself to the training data. Thus, when presented with test data, error values increase because the generalization capacity of the model has been decreased and the model cannot discover the patterns of the test data.”**

“K-fold Cross Validation prevents this by first dividing the total data into k sections and using one section as the test set and the remaining sections as the training set. We train k models, each time using a different fold as the test set and the remaining folds as the training set. Thus, we cover as many combinations of the training and test set as possible as input data. Finally, we take an average of the results of each model and return that as the output. **So, overfitting is eliminated by using the entire data as input, one section (one of the k folds) being left out at a time to use as a test set. A common value for k is 10.”**

**Question:**

**“Can you show me how that works by coding it on a 10 by 10 array of integers? In Python?”**

**Worst Case Answer:**

**…**

**“Ummmmmmmm…..”**

**“Sorry sir, I just studied that in a textbook. I am not sure how I could work through that by code.”**

**(!!!)**

### You Can’t Study Without Implementation

Data science should be studied in the way programming is studied. **By working at it on a computer and running all the models in your textbook, and finally, doing your own mini-project, on every topic that could be important. Can you learn to drive a car by reading about it in a book? You need practical experience! Otherwise, all your preparation is meaningless. That is the point I wanted to make.**

Now, having established this, I assume from here on that you are a data scientist in training who has worked the fundamental details on a computer and is familiar with the basics. You just need the finishing touches on your interview preparation. **If that is the case; here are your topics for mini-projects and experiments! And — interview questions with answers.**

### Interview Practice Resources

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667300120192/iJSXL4xUn.png)

### Python Practice

[https://www.testdome.com/d/python-interview-questions/9](https://www.testdome.com/d/python-interview-questions/9)

This is a site that allows you to sharpen your skills in Python for interviews. There are many more sites like these, all you need to do is Google ‘Python Interview Questions’.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667300121441/PPUzzflkN.jpeg)

### R Practice

Many people know Python, but R is not as commonly known. This [tutorial](https://www.computerworld.com/article/2497143/business-intelligence/business-intelligence-beginner-s-guide-to-r-introduction.html) spans 30 pages that you can work through with your R console to learn the basics. Alternatively, you could try [Swirl](https://swirlstats.com/), which is also highly recommended for beginners.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667300122809/1hmDBk3Lp.png)

### Kaggle

Work through [Kaggle](https://www.kaggle.com/competitions) competitions. No better way to establish yourself in the data science universe.

Also, if you have basic data science skills, try your hand with the hands-on [Kernels](https://www.kaggle.com/kernels) section. Cash prizes awarded every week!

Oh, what are kernels? Kaggle Kernels are online Jupyter notebooks that allow you to **run Python and R code interactively with your browser in the same application without any local processing**. All computation is done on the Kaggle servers.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667300124844/5gzOqdWnO.png)

### Top Ten Essential Data Science Questions with Answers

**1\. What is a normal distribution? And how is it significant in data science?**

The normal distribution is a probability distribution, characterized by its mean and standard deviation or variance. The normal distribution with a mean of 0 and a variance of 1 looks like a bell, hence it is also referred to as the bell curve. The central limit theorem makes the normal distribution ubiquitous in data science. In its essence, the central limit theorem states that data values tend to be attracted to the normal distribution shape as the number of samples is increased without limit. This theorem is used in data science nearly everywhere, because it gives you an ‘expected’ value for an arbitrary dataset that has, say, n = one thousand samples. As n increases, if the data is normally distributed, the shape of the graph of that attribute will tend to look like the bell curve.

**2\. What do you mean by A/B testing?**

An A/B test records the results of two random variables or hypotheses (depending upon the scenario) and compares the rate of success or accuracy for the variable being in the state of A or the state of B. This often tells us which feature should be used to build a machine learning model. It is also used to select which model to use in the first place. A/B testing is a general concept that can be applied to nearly every system.

**3\. What are eigenvalues and eigenvectors?**

The eigenvectors of a matrix that is non-singular (determinant not = 0) are the values associated with linear transformations of that matrix. They are calculated using the correlation or covariance matrix functions. The eigenvalues are the values associated with the strength or the degree of a linear transformation (such as bending or rotating). See **Linear Algebra by Gilbert Strang** (online ebook) for more details on their computation.

**4\. How do the recommender systems in Amazon and Netflix work? (research paper** [**pdf**](https://s3.amazonaws.com/academia.edu.documents/33324004/Explanations_in_Recommender_Systems_Overview_and_Research_Approaches.pdf?AWSAccessKeyId=AKIAIWOWYYGZ2Y53UL3A&Expires=1540381486&Signature=Fr9Dm6Ty87ug6sGq5w9KdFYzVAs%3D&response-content-disposition=inline%3B%20filename%3DExplanations_in_Recommender_Systems_Over.pdf%29)**)**

Recommender systems in Amazon and Netflix are considered top-secret and are usually described as black boxes. But their internal mechanism has been partially worked out by researchers. A recommender system, predated by expert systems models in the 90s, is used to generate rules or ‘explanations’ as to why a product might be more attractive to user X than user Y. Complex algorithms are used, which have many inputs, such as past history genre, to generate the following types of explanations: **functional, intentional, scientific and causal**. These explanations, which can also be called **user-invoked, automatic or intelligent**, are tuned by certain metrics such as **user satisfaction, user rating, trust, reliability, effectiveness, persuasiveness etc**. The exact algorithm still remains an industry secret, similar to the way that Google keeps the algorithms that perform PageRank secret and constantly updated (500–600 times a year in the case of Google).

**5\. What is the probability of an impossible event, a past event and what is the range of a probability value?**

An impossible event E has P(E) = 0. Probabilities take on values only in the closed interval \[0, 1\]. The probability of event that is from the past is an event that has already occurred and here P(E) = 1.

**6\. How do we treat missing values in datasets?**

A categorical missing value is given its default value. A continuous missing value is usually assigned using the normal distribution, or the measures of central tendency like mean, median and mode. If a feature has less than 20% available data, the recommendation is to delete that feature from the model.

**7.** **Which is faster, Python or R?**

Python is considered to be moderately medium-paced since C++ is much faster for all purposes. Besides which, Python is an interpreted and not a compiled language. Python language is implemented in C to speed up execution time. R, however, was designed by statisticians, not computer scientists, and is much slower than Python.

**8\. What is Deep Learning and why is it such a popular buzzword in the machine learning field right now?**

For many years, until around 2006, backpropagation neural networks had just three layers — one input, one hidden and one output layer. The problem with this model was that since it used **gradient descent and the backpropagation algorithm,** the neural nets had a tendency to be attracted towards the local minima in the hyperplane that represented the dimensions of the input features. Thus, NNs could not be used for many applications optimally, since they could only find a partially optimal solution. In 2006, Geoffrey Hinton et. al. published a research paper that showed that multilayer neural networks could overcome the problem of local minima since, in thousands of dimensions, local minima are statistically so rare as to never be found in the back-propagation process (saddle points are common instead). Deep learning refers to neural nets with 3 or more (even 10) hidden layers. They require more computational power and were one of the reasons that GPUs started to be used by the machine learning community for implementation of deep learnings NNs. Since 2010–2012, deep learning has been applied to nearly every single technology domain, and the models have been highly accurate and successful in all areas from speech recognition to playing the Japanese game of Go.

### Enjoy Your Work!

To finally sum up, I have to say, **enjoy your work.** You will be much better at what you love than something that is glamorous but not to your taste. Artificial Intelligence, Data Science, Software Development and Machine Learning are very much in my preferred line of work, and my hope is, that it will be in yours too. **Don’t just read the text, work out the code on your systems or on Kaggle. That is how to best prepare for interview questions. Only practice at your computer (preferably on Kaggle) will give you true confidence on the day of your interview.** That is true expertise — practice making perfect. **Enjoy data science!**

#### Support My Writing

**Support my writing.** **Join Medium** to read the best content on the web through the link below and 50% of your membership fee supports me every month. A sincere thanks to all my wonderful subscribers who help me and support my writing every month.

Join Medium with my referral link below — Thomas Cherickal

[**https://thomascherickal.medium.com/membership**](https://thomascherickal.medium.com/membership)

God bless.

#### Coffee!

If you enjoyed this article, do buy me a coffee every month for 2 USD:

[https://ko-fi.com/thomascherickal](https://ko-fi.com/thomascherickal)