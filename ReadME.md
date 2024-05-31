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
- [Additional Resources](#resources)


## Prerequisites
1. Install [VSCode](https://code.visualstudio.com/download)
2. Install [Node.js](https://nodejs.org/en/download/package-manager/current)

## How To Get Started

## Fundamental Practices

[Performance vs Scalability](https://blog.professorbeekums.com/performance-vs-scalability/)

Here is a great resource for understanding the difference between Performance and Scalability. 

The article gives a great example comparing the task of checking out at a grocery shop to messaging queues. When we are vertically scaling in the example, it does not solve the issue of heavy load because our throughput has not increased. Even if we added caching (providing a repeat customer with the same receipt to process within seconds), it only covers a small percentage of customers(data) ignorant to data changing or new data coming.

Instead of caching, horizontally scaling by adding more cashiers and workers to check out each customer allows the performance to be close to constant.

The author also mentioned the importance of adding a messaging queue, for each message to be processed in an orderly fashion.

When the amount of customers is increasing, we should scale horizontally to keep performance at a constant rate.

## Resources

[RoadMap System Design](https://roadmap.sh/system-design) - This is a fantastic roadmap for learning the fundamental skills of System Design

[InterviewReady's System Design Resources](https://github.com/InterviewReady/system-design-resources) - A load of resources here so it may be overwhelming. I recommend using this resource to dive deeper into a subject you may be unclear about

[Microsoft Azure Cloud Design Patterns](https://learn.microsoft.com/en-us/azure/architecture/patterns/) - This is another fantastic resource to learn all the fundamental Design Patterns
