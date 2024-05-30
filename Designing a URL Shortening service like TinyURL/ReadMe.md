# TinyURL

## Table of Content
- [Identifying the System We are Designing](#identifying-the-system-we-are-designing)
  - [Why Shorten URLs](#why-shorten-urls)
  - [What this does for us](#what-this-does-for-us)
  - [Immediate Concerns](#immediate-concerns)
  - [Clarifying Requirements and Goals of the System](#clarifying-requirements-and-goals-of-the-system)
  - [Estimating Storage Requirements and Constraints](#estimating-storage-requirements-and-constraints)
- [Designing the API](#designing-the-api)
- [Designing the Database](#desigining-the-database)

## Identifying the System we are designing

### Why Shorten URLs?

#### Problem

Extremely Long links waste a lot of space, when displayed and stored it will cost more resources for each additional character over many years.

#### Solution

Shorten the lengthy URLS that will cut down the size significantly.

#### Example:

Long:
[http://thelongestdomainnameintheworldandthensomeandthensomemoreandmore.com/](http://thelongestdomainnameintheworldandthensomeandthensomemoreandmore.com/)

Shortened:
[https://tinyurl.com/bdfzddz8](https://tinyurl.com/bdfzddz8)

###### (Question this -> Would you click on the shortened link above? How can you be sure it is not a malicious site to which you will be redirected?)

### Purpose

This allows us to optimize links, add trackable metrics on links, and hide affiliated URLS

### Immediate Concerns

My initial concerns in designing this system would be:
- What if there is malicious intent in the original URL?
- What if another user shortens the same lengthy URL? Will this generate a new shortened URL? Duplicates?
- How will the Shortened URL be valid for?
- What happens if the Server goes down for the Shortened URL?
- Security?
- Database?

### Clarifying Requirements and Goals of the System

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

### Estimating Storage Requirements and Constraints

We can evaluate the ratio of read and write for this type of service by the core functionality. It is always best to consult the interviewer to ensure your evaluation is true.

1. Ask the Interviewer what is the expected traffic for the ratio of read: write for this service. For each link created what average estimate of viewers should I use to gauge Storage requirements?
2. Ask the Interviewer for an estimate of Traffic for new URL shortenings per month
3. Calculate the amount of write/sec
4. Calculate the amount of read/sec
5. Calculate the amount of URLs Shortened in 5 years
6. Ask for a ballpark storage size to calculate the total storage we need in 5 years.
7. Calculate write incoming data per second
8. Calculate read outgoing data per second
9. Hotloading URLS 80% 20% Pareto principle 20% of the URLs will drive 80% of the traffic. Calculate how much storage we need to cache hot URLs.

Finally, after all calculations, we have a High-Level Estimate for the service:

```
URLs Written: X (KB, MB, GB, TB/s)
URL Redirections: X (KB, MB, GB, TB/s)
Incoming data: X (KB, MB, GB, TB/s)
Outgoing data: X (KB, MB, GB, TB/s)
Storage for 5 years: X (KB, MB, GB, or TB)
Memory for cache: X (KB, MB, GB, or TB)
```

## Designing the API

## Designing the Database


