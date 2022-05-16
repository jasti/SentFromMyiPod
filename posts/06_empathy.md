---
title: Does Your API Empathize With Its User?
description: Does Your API Empathize With Its User?
date: 2014-04-27
tags: Code
layout: layouts/post.njk
---

I am appalled at the difference in API usability between an API developed for B2B (Business to Business) vs. one developed for B2C (Business to Customer). A good example of a B2B API in the finance world is the <a href ="http://www.swift.com/products_services/by_type/messaging/index">15022 swift messaging</a> (primarily used for communication between two financial institutions) which look like a 5 year old's half eaten bowl of spaghetti. Compare that to a B2C API like  <a href ="https://parse.com/docs/rest">Parse</a> (a Backend as a service application) which has a beautifully designed API which is a pleasure to work with as a developer. 

The biggest reason for this huge disparity? I call it developer empathy. 

Parse's API developer is able to empathize with her customer base and ask an important question - "What would I like to see in this API?". This is primarily because most technology companies build products that the software engineers can inherently understand. Contrast that to a finance company. A business analyst is usually involved who "translates requirements" for the developer. The developer can't relate to the product anymore. The task becomes a chore for the developer and chances are that he won't be as motivated to build a kick-ass product. Not to mention the things that get lost in translation when you start involving a business analyst. 

As an aside, I strongly feel that everybody who considers themselves part of the tech department must be able to program. Programming languages are so easy nowadays and there are so many resources online that anyone should be able to at least checkout, change some lines of code and commit to staging. Heck, maybe even prod. This reduces the back and forth cycle of "Can you please restrict this report to weekdays?" type of questions by at least half. Allows both developer and BA to be on the same page and allows tighter iterations of the product. Anyway, I digress.

Consumer-facing tech companies have begun to <a href="http://en.wikipedia.org/wiki/Eating_your_own_dog_food">dog food</a> two types of products: <br>
1. Building products which the software engineers themselves could be users of. E.g. <a href ="https://www.gmail.com">Gmail</a>  <br>
2. Hardware and internal tools. E.g <a href ="https://cloud.google.com/ ">Google Cloud </a> <br>

The second type of dogfooding is interesting. Making products like Google Cloud and Amazon AWS available for public developers / customers, the companies are inherently making these businesses client facing / sexy. They turn into revenue generating businesses. As an added bonus, this gives the company a QA base that is as big as their customer base. Internal software developers empathize with the products they build. 

Products obviously need to get built even if they are not customer facing and companies need to start thinking about introducing developer empathy in the B2B world. The solution is to simplify standards and treat the end consumers of the businesses not as businesses, but as individual developers. 

---