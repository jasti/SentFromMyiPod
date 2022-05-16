---
title: Real World Big Data Techniques
description: Real World Big Data Techniques 
date: 2014-08-31
layout: layouts/post.njk
---

Big data has become a big buzzword. There are a ton of articles that come to the conclusion that big data = big profits for firms that are willing to use it, but don’t explain the <i>how</i> part. 

Most articles explain solutions for big data problems by using basic statistics to analyze large amounts of data. By basic statistics I mean counts, means, medians, standard deviation. This is not new and a number of firms have been doing this since the late 90’s. This is called analytics. The difference today is the large amount of digital information being generated per second as well as the technology advances in software and hardware to tackle these large volumes of data.

In my opinion there are much more interesting uses of big data to uncover hidden potential and revenue-generating strategies of a firm’s business. And that is data mining / data science, a class of machine learning algorithms that are often overlooked in traditonal journalism. 


<center><img src="/images/blog/bigdata/ai.png"/></center> 

Machine learning is the ability to train a machine with data using algorithms.


It has been often <a href = 'http://anand.typepad.com/datawocky/2008/03/more-data-usual.html'>discussed</a> that more data is better than a complex algorithm. My goal is to look at simple real world applications of data science using big data by employing different techniques, which addresses the <i>how</i> part of the big data = big profits equation.
 
In order to understand the techniques, it is important to understand what a model is.

A model is an entity that allows you to capture regularities in data. The way one constructs a model is by identifying attributes of a data set that are relevant to the analysis and use them (through feature extraction) to construct a model. If you are doing email analysis, your features could be sender location, email body text sentiment, etc.

<center>
<br>
<blockquote>
Machine Learning Model = Data + Algorithm
</blockquote>
</center>
<br>


<h3>Classification | Gmail Email</h3>
Gmail (and most other email software) has the ability to detect if the email you received is from your friend or from that Nigerian teenager who is phishing (fishing?) with a new scam. To do this Gmail uses a technique called <b>Classification</b>. Gmail parsed all emails from the beginning of time and built a model. The next time a new email arrives, the features of the new email are input into the model in real-time and a decision is made to <i>classify</i> if the new incoming email is spam or good (ham?).

<h3>Regression | Zillow Housing Prices</h3>
Regression is used in situations where a system attempts to predict a numerical value. Zillow uses this by looking at other similar houses by building a model using features like number of bedrooms, location, school district, etc and estimates (Zillow calls this <a href = 'http://www.zillow.com/zestimate/'>Zestimate</a>) the price of a house.

<h3>Similarity Matching | Amazon Recommendations</h3>
Similarity matching can be used to find similar entities of a product.  We’ve all seen the “People who bought..” section on Amazon. The way Amazon makes these suggestion is by not just using empirical past transactions but also doing similarity matching of product features. Another interesting example is how IBM was successful in identifying similar firms, so it could put its salesforce to best use while selling a product. 

<h3>Clustering</h3>
Clustering attempts to group entities together that are similar to each other but <i>not driven by any specific purpose </i>. I’ve found clustering useful during the initial phases of exploratory data analysis. Data scientists usually start with this algorithm to tackle ‘You don’t know what you don’t know’ scenearios.

<h3>Data Reduction  | Netflix Genre Prediction</h3>
Netflix uses this as one of the many algorithms while trying to make genre recommendations for users based on large user movie watching history. This algorithm attempts to take a large set of data and replace it with smaller amount data which more or less contains the most important identifiable information in the larger data set. This is also known as noise reduction. Like clustering, this is also one of the first techniques applied when exploring data. 

<h3>Co-occurrence grouping | Walmart & Target Shelf Placement</h3>
Co-occurrence grouping is used by by large retailers like Target and Walmart to place items on shelves next to each other. This is similar to clustering, but more specific. It allows to identifying items that were purchased in the same transaction. An obvious example is, if you bought gin, you are likely to buy tonic as well. <a href = 'http://www.forbes.com/forbes/1998/0406/6107128a.html'>Beware</a> of the false positives you can uncover using this algorithm. 

<h3>Profiling | Chase Credit Card Fraud Detection</h3>
Almost all banks like Bank of America, Chase, etc. have fraud detection on credit card purchases setup using profiling. Profiling is used to establish behavioural norms of a consumer. So in cases where an event occurs outside of the norm, the individual is alerted. 

<h3>Link Prediction | Linkedin People You May Know</h3>
Linkedin is famous for introducing the <a href = 'http://data.linkedin.com/projects/pymk'>‘people you may know' feature</a>. A  graph is constructed to form the relations between all the individuals (nodes), and if two people have a number (say 10) of common friends, they probably know each other.

That’s it for the whirlwind tour of big data using data science and goes without saying that one could write a book about each of these topics. My goal is to show real world applications of big data using machine learning and data analysis. The next time the journalist talks about “big data,” it might be interesting to consider not just the ‘what’ but the ‘how.’


---