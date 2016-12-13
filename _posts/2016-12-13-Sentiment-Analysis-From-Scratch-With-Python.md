---
layout: post
title: Sentiment Analysis From Scratch with Python.
date:   2016-12-13
desc: "二零一六中秋节的一些随谈"
keywords: "Sentiment Analysis, tweets, Python, Machine Learning"
categories: [SA]
tags: [blog]
icon: fa-bookmark-o
---

This is a demonstration of sentiment analysis using a NLTK 2.0.4 powered text classification process. It can tell you whether it thinks the text you enter below expresses positive sentiment, negative sentiment, or if it's neutral. Using hierarchical classification, neutrality is determined first, and sentiment polarity is determined second, but only if the text is not neutral.