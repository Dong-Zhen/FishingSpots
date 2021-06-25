# Abstract

------------

Fishing contributed 2.4 billion dollars and supported 10,964 jobs in New York State in 2017. Most of the state's anglers fish in freshwater bodies. In the New York State DEC's 5 year angler 2017 survey, they learned that in that 42% of anglers ranked information on how and where to fish as the number one action to increase their fishing participation. Since it is essential for NYS to attract and retain anglers, I propose scraping the top 2 New York fishing forums
to perform nlp and unsupervised learning to find relevant information from thousands of active fishermen. The topics found will form the basis of this year's informative material to attract and retain anglers.

------------
### Design

Fishing evolved from a life sustaining skill to a hobby. As a result, many people in cities do not have the starting fishing knowledge to begin their journey. There are all sorts of books, some outdated, some bias that could lead an amateur fishermen to many different options and confused on where to start. My hope is to clear up this confusion by extracting the common talking points from active practioners on important components of fishing.

The key components to fishing is understanding where and when to go for a certain species of fish, what bait to use, an understanding of how weather affects fishing. Then there is the main tool, the rod and its necessary attachments: reel, spool, line, hook or lure, bait.

This directed my preprocessing to find the most relevant information for New York anglers and a topic model that will give an overview of the key components.

### Data

The top two online New York fishing forums are NYangler and NyBass, each contains thousands of users. Forums are the best way to learn from a large group of individuals with varying opinions and not from one individual. It provides the least bias and richer topics. Also most people who want to share their experiences on forums tend to be passionate or has experience in what they are talking about.

Noticeably, forums tend to have many different threads and I focused specifically on fishing report and technique threads. From these threads I extracted almost 30,000 posts with an average length of 3,200 words to form my corpus.

### Algorithmn 

I used TDIF from sklearn to vectorize the corpus to extract the weight of each word on the entire document and then performed topic modelling using NMF. What NMF did was create topics based of words that occur together in the documents of the corpus. Each topic has the weight of the words that make up the topic, so it's easier to interpret which words had the impact on a specific topic. 

After I used TDIF and NMF on the entire corpus, I split up the corpus by seasons and perform the same vectorization and topic modeling again to understand the topoics for each season.

Noticeably the post titles of the corpus contained fishing species and location topics while the contents in the post contained information on how to catch the fish such as the type of rod and its attachments and some information on the weather.

### Conclusion

I was able to make concise suggestionis based of the topics of post title and post content. For example in the spring, anglers should check out lake saratoga with a light shimano spinning rod with a braided line, jig fishing lure, and worms as bait to catch species of bass. To be certain that these topics are relevant, I spent a day researching these recommended components and it turns out that saratoga is a top-notch fishery and known for its bass. Shimano rods are also featured in many top 10 rod articles, braided lines have become popular over the last decade, and worms are great bait year round. Looks like you have enough information to begin a fishing trip, time to go fishing!

### Links

- [Final Code](https://github.com/Dong-Zhen/PredictingFlightDelays/tree/master/Code)
- [Presentation](https://github.com/Dong-Zhen/PredictingFlightDelays/blob/master/Flight%20Delays.pdf)
- [Write Up](https://github.com/Dong-Zhen/PredictingFlightDelays/blob/master/Final%20Write%20Up.md)
- [Research](https://github.com/Dong-Zhen/PredictingFlightDelays/tree/master/Code)
