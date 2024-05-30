# Interactive System Design Practice
## The goal

  I want to focus on a more interactive JavaScript learning experience with System Design. To supplement reading the Grokking System Design Interview, I want to design the system visually using console commands, tests, and simpler indicators of why **A** **B**, and **C** are implemented and what is it doing.

Here you will find steps for Caching, Load Balancing, and Partitioning will timeout for 4-5 seconds console logs what is happening in the moment and why we have it in place.

Following the interactive design is a comprehensive readme that will break down the pros and cons, the thought process, and the alternatives of each design.

Currently, I'm working with examples from Grokking the System Design Interview but will find more content on Cloud Design Patterns from Azure in the future.

## Table of Contents

- [Prerequisites](#prerequisites)
- [How To Get Started](#how-to-get-started)
- Source: Grokking the System Design Interview
  - Easy: [Designing a URL Shortening service like TinyURL](https://github.com/chitangchin/InteractiveSystemDesign/tree/main/Designing%20a%20URL%20Shortening%20service%20like%20TinyURL)
- Source: Microsoft Azure Cloud Design Patterns


## Prerequisites
1. Install VSCode
2. Install Node.js

## How To Get Started

## General Step-by-Step Guide for designing a system

Understanding the Case Scenario and Asking

Clarifying Questions

Understanding the workflow and User story

focus on designing the backend front or both?

Define the APIs

postTweet(what data needs to be passed)
...

estimating the scale of the system
scaling partitioning load balancing and caching

what scale is expected? tweets number of tweet views timeline generations per sec, etc

how much storage will we need?
each tweet is unique to the storage size of photos and videos

network bandwidth usage are we expecting? how to manage traffic and balance load between servers

defining data model
how data will flow among components

user:
Tweet
user follow:
FavoriteTweets

NoSQL? or MySQL?

what kind of block storage should we use to store photos and videos?


