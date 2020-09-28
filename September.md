### Lun. 28/09/2020
It's been ages since my last commit, but i was really over with exams and work. I did a mongoDB integrator in order to add values retrieved using the id from the tweets. It's quite slow and probably has has some limitations, but is a beginning. So i'll plan to fix the mongodb and the data pretty soon, and then there will be times to add analysis. Hope to finish by the time!

### Ven. 11/09/2020
[https://github.com/amaiya/ktrain](KTRAIN) Seems exactly what i was looking. No time today for code, but i'll probably start from here!

### Gio. 10/09/2020
Finished first script for SentimentAnalysis: is very lightweight and seems to work fine. I used Vader and for non-english input i used a translation: btw i need to check the request rate. 
The next step is to retrive in batch the tweets in MongoDB and then compute sentiment analysis. 
I google for neural approaches for sentiment analysis but using BERT or other pre trained means to reduce the problem to a classification task (like on movie review, sentiment analysis is associated to predict the value of the review). This can be exploided (using words to words approached in order to check if a given words change the review in positive or in negative) 'but i dont need to reinvent the wheel soooo.
I also need to check the dicts used by Vader. If i dont like it or its not usable (no domain specific), i'll fork and customize everything.
[Github repository for Vader](https://github.com/cjhutto/vaderSentiment)

### Mer. 09/09/2020
Did a call with supervisor for the direction to take in order to do the analysis, and we agreed on follows:
1. Data ingestion for preprocessing and ingest text (in memory)
2. Apply some sort of topic modeling 
3. Apply some sort of Social Network Analysis
4. Find good resources for sentiment analysis tool (probably [VADER](http://comp.social.gatech.edu/papers/icwsm14.vader.hutto.pdf) ). 

Essentialy what i have to come up with is a robust, flexible, real-time data ingestor for sentiment, topic modeling and social network analysis. 
Probably three distinct softwares.
