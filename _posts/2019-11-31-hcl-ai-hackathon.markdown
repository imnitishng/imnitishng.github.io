---
title: "HCL AI Hackathon Lucknow Experience"
layout: post
date: 2019-11-31 15:10
tag: nlp
image: ../assets/images/hcl2.gif
headerImage: true
projects: false
description: "My Experience"
category: blog
author: Nitish Gupta
externalLink: false
---

Hello World!
This is my first ever blog post. Like literally the first ever in my life. Never been into blogging but after lurking around the internet for quite some time I know how important it is to have an online presence in the world. Recognition is important.

So this will be a late blog post but i would still like to share my experience on the HCL Hackerearth AI Hackathon which happened on 1st and 2nd November at the HCL IT City campus. The Hackathon involved 2 main themes and an extra open innovation. The organization and amendments done for participants were top notch. We had no problems whatsoever and were looked after for the whole 24 hours that the Hackathon went on for. 
Jumping onto some technical details, so for me I was solo, did not find a suitable team member plus i have no contacts with people genuinely interested in hackathons or having the skill set to be of some use. Plus being a non Computer Science Undergraduate it's hard for me to find a teammate of some actual use. People from my college show little to no interest in hackathons or competitions, getting spoonfed in the college with whatever crap they teach (i hate electronics) is all they desire for. Enough of that, he finally had talks with one of my friends who was an iOS developer, he agreed on providing a front end interface for the product while managing all the backend.
I chose the theme Sentiment analysis from the 3 they proposed (mistake). Enough of introduction, let’s dive deeper into technical details.

So the project was basically divided into 3 crucial parts -
- Scraping data
- Creating Model
- Deploying and UI

# Scraping
Scraping data was the most time consuming work I did for the project, I beautiful soup and Selenium to do the job and build 2 scrapers,  one for Google Maps and another for TripAdvisor, scraping data from the web is a time consuming job that’s for sure. 
The scripts, alongwith the scraped data can be found in the github repo here [imnitishng/scrapers](https://github.com/imnitishng/sentiment_analysis_insights_tourist/tree/master/scrapers).

# Creating the Model
Creating the Model was the best experience I had, I used fast.ai to build a language model, this language model was trained on WikiText-103 dataset, so we can infer that this model "knows" what english language is, we just need to transfer learn over it in order to see how it performs on unseen tourist review data.
So the data we scraped from websites was used to transfer learn, over our language model to create a classifier out of it. All the data preprocessing and model training code is provided in the [imdb-fastai.ipynb](https://github.com/imnitishng/sentiment_analysis_insights_tourist/blob/master/imdb-fastai.ipynb) file. Training of classifier was done on a mixture of IMDB movie reviews and tourist scraped data over a fastai language model with a promising 93.9% accuracy with just ~2 hrs of training on Tesla P100 from Kaggle. 


# Deploying and UI
For deploying I had the idea to publish the app on AWS, but due to time restirictions I had to use Kaggle instead. Kaggle has a great and easy UI to interact with code and get work done. The final hours were in and with no sleep for almost 20 hours I built an API for generating rich charts of the keywords and insights from the huge data, the topics and insights were extracted from the data using LDA.
Have a look at the Jupyter Notebook [imnitishng/presentation](https://github.com/imnitishng/sentiment_analysis_insights_tourist/blob/master/presentation-notebook.ipynb)

# Verdict.
- Hackathon was great
- Arrangement was great
- Learnt a lot
- I do believe they had to explain the problem statements better.