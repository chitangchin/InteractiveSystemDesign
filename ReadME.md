# Interactive System Design Practice

## The goal

<p>
  I want to focus on a more interactive learning experience with System Design. Rather than reading the textbook for Grokking System Design Interview, I want to design the system using console commands, tests, and simpler indicators of why a b and c are implemented and what is it actually doing.

Here you will find steps for Caching, Load Balancing, and Partitioning will timeout for 4-5 seconds console logging what is actually happening in the moment and why we have it in place.

Following the interactive design is a comprenehsive readme that will breakdown the pros and cons, the thought process and the alternatives of each design.

Currently I'm working with examples from Grokking the System Design Interview, but will find more content on Cloud Design Patterns from Azure in the future.
</p>

The format:
<ul>
  <li>Source</li>
  <li>Difficulty</li>
  <li>What System we are designing</li>
</ul>

## Table of Contents

#### Source: Grokking the System Design Interview

<ul>
  <li>Easy: Designing a URL Shortening service like TinyURL</li>
</ul>

#### Source: Microsoft Azure Cloud Design Patterns

## General Step by Step Guide for designing a system

Understanding the Case Scenario and Ask

Clarifying Questions

Understanding the workflow and User story

focus on designing the backend or frontend or both?

Define the APIs

postTweet(what data needs to be passed)
...

estimating the scale of the system
scaling partitioning load balancing and caching

what scale is expected? tweets number of tweet views timeline generations per sec, etc

how muhc storagew will we need?
each tweet is unique to the storage size photo and videos

network bandwith usage are we expeciong? how to manage traffic and balance load between servers

defining data model
how data will flow among compnents

user:
tweet
userFollow:
FavoriteTweets

NoSQL? or MySQL?

what kind of block storage should we use to store photos and videos?


