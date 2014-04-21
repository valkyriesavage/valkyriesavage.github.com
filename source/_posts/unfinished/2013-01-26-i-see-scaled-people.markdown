---
layout: post
title: "pyramids of people"
date: 2013-05-30 20:14
comments: true
published: false
categories: [computer vision, hci, semantic scene recognition]
---

During Jitendra Malik's seasonal offering of CS280:Computer Vision, <a href="http://eecs.berkeley.edu/~shiry">Shiry Ginosar</a> and I teamed up on an HCI-inspired computer vision project.  Our idea was simple: we wanted to try using person density and action context for the purposes of scene recognition.

First of all, it's important to know what scene recognition even means.  In essence it's a task for a computer to take a photograph of a "scene" (think office, forest trail, boat, church, etc.) and give back an answer of what it thinks the photograph is of.  Typically this is done after training the computer by giving it many many labeled photographs of scenes, so that it can learn how to tell them apart.

Think about a few scenes in your head for a moment.  How many people did you see last time you were at the beach, and what were they doing?  Now compare that to a scene in an airport, how many people were there, and what were they doing?  How about the last family dinner you had?

We thought it seemed like a reasonable amount of signal, in particular when taken with the traditional methods of scene recognition (one of the most popular is location and number of lines of particular orientation).  To make it stronger, we elected to try out using spatial pyramids: basically this tells you not only how many people are in the scene, but where in the scene they are.  This would show a difference between, e.g. the airport where many people are roughly evenly distributed and the beach where people may be clumped together in their groups of friends.

For our semantic scene recognition task, we needed a dataset and some kind of algorithm.  For the dataset, there are fortunately multiple large and open labeled scene databases for use by academics (or anyone who's interested).  We settled on XXXXXXXX? because we wished to compare our results to a XXXXXXXXX paper that uses it.  Algorithm-wise, we had the good fortune to build off of XXXXXXXX poselets, which was developed in-house at Berkeley by the CV group.

The confusion matrix of our results is shown below:

XXXXXXXX

Obviously, we could have done better.  We believe the problem was that we never got the thing running on the UCB CV cluster, so we had to settle for training and running it on tiny pieces of the ideal training set.  Another issue was that not all the photos in the database contained people, so the training data we did use wasn't necessarily dense in information.  We've been talking about finishing this project up for months, but have never made the time to do it... so it's still exciting, low-hanging fruit waiting for someone to pick it up!
