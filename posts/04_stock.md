---
title: Equity Stock Predictor
description: Equity Stock Predictor
date: 2014-03-21
tags: finance
layout: layouts/post.njk
---

Do you want to know if there is a correlation between the news on a company and performance of the company’s stock in the market? Enter Stock Predictor - An open source project I authored that listens on Reuters via a twitter handle and screens the articles for positively or negatively correlated news for stocks you are interested in. 

Based on the sentiment analysis of the news article, the program will suggest to take a direction on the stock. For example, if Reuters publishes a leak about Apple launching the iWatch and what a huge success it will become, the app will calculate a positive sentiment and mark it closer to 1. Depending on the exact sentiment score, the app will recommend buying a large number of stocks when the number gets closer to 1 and the app will recommend selling the stocks when the sentiment score is closer to 0. i.e shorting the stock.

You can find the project  <a href ="https://github.com/jasti/Stock-Predictor">here</a>.  

Give it a spin, fork it and send me a pull request if you think something can be improved here. My vision for this a poor man's high frequency trading app. All that this would be missing is a broker who is willing to give you electronic access actually trade electronically trade on a market. This type of access is called leased lines and firms spend quite a bit to have this kind of access. At the very least, you can simulate your paper profits of stocks you are interested in and who doesn't like doing that!


---