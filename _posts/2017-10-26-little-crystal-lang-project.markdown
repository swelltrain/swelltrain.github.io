---
layout: post
title:  "Little Crystal Lang Project"
date:   2017-10-26 06:37:22 -0700
---

## Background
I have been following crystal-lang for a little while and thought it would be fun to play around with it.  I love the syntax of ruby and I love the idea of something that runs even faster.

I came up with a little project that seemed like a good fit:  build a word cloud of my google hangouts conversation history with my girlfriend.  So I needed to parse a big json file into a set of words.

## Thoughts
Coding in Crystal was a joy.  Overall I feel like the language is very well balanced.  It's a difficult metric to convey, but it feels like it sits in a very sweet spot.

I probably spent more time hunting around on the internet looking for a good writeup on the format of the google hangouts json file than I did coding.  I finally just looked at someone else's python code and loosely followed along.

Most of my tests were pretty stupid because I was feeling my way through the language (ie: does this getter method actually work).  But it felt balanced and nice because testing in crystal is so easy.  And Crystal's speed turned out to be a real asset because it helped me to iterate as I coded.  I could write small tests and run them very quickly, and also run everything against the full file and get results back quickly enough that I never lost flow.

It helped that I am comfortable with Ruby syntax, but coding in crystal felt very fun and rewarding.  And GF and I had a lot of fun looking at it and reviewing the words and conversations that reflect our shared vocabulary.  It was also nice to see that we "HA HA GOOD LIKE YEAH SORRY LOVE YES THINK" a lot together.

Here is the code-- warts and all :)
[https://github.com/swelltrain/hangouts](https://github.com/swelltrain/hangouts)

It just spits out all the conversations with very little formatting.  I piped it to a file and fed it to [wordclouds.com](https://www.wordclouds.com/)

Some additional nice-to-haves would be to stem the words using [porter-stemmer](https://tartarus.org/martin/PorterStemmer/c.txt).  This would be an easy way to learn how to call C from Crystal.
It could also be neat to apply a tone analysis but I'm not sure what tools are available for that.

## Part Of The Results

![]({{ "/assets/word_cloud.png" | absolute_url }})
