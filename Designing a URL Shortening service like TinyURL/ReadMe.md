# TinyURL

## Table of Content
- [Why Shorten URLs](#why-shorten-urls)
- [What this does for us](#what-this-does-for-us)
- [Immediate Concerns](#immediate-concerns)
- [Clarifying Requirements and Goals of the System](#clarifying-requirements-and-goals-of-the-system)

## Why Shorten URLs?

### Problem

Extremely Long links waste a lot of space, when displayed and stored it will cost more resources for each additional character over many years.

### Solution

Shorten the lengthy URLS that will cut down the size significantly.

### Example:

Long:
[http://thelongestdomainnameintheworldandthensomeandthensomemoreandmore.com/](http://thelongestdomainnameintheworldandthensomeandthensomemoreandmore.com/)

Shortened:
[https://tinyurl.com/bdfzddz8](https://tinyurl.com/bdfzddz8)

###### (Question this -> Would you click on the shortened link above? How can you be sure it is not a malicious site to which you will be redirected?)

## What this does for us

This allows us to optimize links, add trackable metrics on links, and hide affiliated URLS

## Immediate Concerns

My initial concerns in designing this system would be:
- What if there is malicious intent in the original URL?
- What if another user shortens the same lengthy URL? Will this generate a new shortened URL? Duplicates?
- How will the Shortened URL be valid for?
- What happens if the Server goes down for the Shortened URL?
- Security?
- Database?

## Clarifying Requirements and Goals of the System

Ask the interviewer these questions:

- **What** are the Functional Requirements you are looking for in this app?
- **What** are the Non-Functional Requirements?
- **What** are the Extended Requirements?
- **What** do you like for me to design? The Backend or Frontend or Full stack system?

(I'd like to know what the interviewer wants from me.)

According to Grokking System Design book, the interviewer is looking for the following:

**Functional Requirement**
1. When the service consumes a URL it will output a shortened and Unique link. We can call this a *short link*
2. The *short link* will redirect users to the original link
3. The user should have the option to customize the short link
4. Provide a default life span for links, and let Users specify the life span.

**Non-Functional Requirement**
1. A highly available system
2. Minimal Latency on redirection of Short Links
3. Shortened Links should be unpredictable

**Extended Requirements**
1. Analytics, Metric Tracking
2. Service can be consumed as a REST API for other services

## 



