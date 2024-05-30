System design Approach

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


