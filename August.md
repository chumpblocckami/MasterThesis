### Lun. 17/08/2020
Did testing and refined which metadata to get from stream. Also decided on which languages focusing for the analysis: **ENG ITA ESP**.

### Dom. 16/08/2020
Presentation and reading of [SOTA MODELS](https://paperswithcode.com/sota)

### Sab. 15/08/2020
Ferragosto

### Ven. 14/08/2020
Testing and stuff on lab's computer

### Gio. 13/08/2020
Today was a good day! Migrated the architecture on Lab Server and it actually works in the first glance! I had trouble to start MongoDB in localhost since there were running istances of it in other users, and it probably has some conflict. btw every worked fine, a small step to the right direction! :)
Today i'll finish the test, i'll think about what to download more (other text features or stuff like that) and i'll probably start the ingestion on August 15th.

### Mer. 12/08/2020
Updated and optimized redis architecture for tweets. Now it's lightning fast (storing 1.5k tweets every updates), we can also add the in-memory preprocessing before store it in the mongodb cluster.

### Mart. 11/08/2020
Did subscriber/consumer redis architecture for tweets.

### Lun. 10/08/2020
Installed Redis on Google Colab and experiment with it. Finished the LDA on english tweets and looked for NLP Multilingual libraries, found [HANLP](https://github.com/hankcs/HanLP). What i figured out is that i need to preprocess every tweet BEFORE adding it to MongoDB, so i need something that will queque the stream, such as Redis (that is also good for exactly once). So essentialy i process then commit to db, saving time when i'll analyze the tweet. Another idea will be to get with Redis from MongoDB, but i need to study more the architecture.
UPDATE: Windows is no long supported by Redis (lol).

### Dom. 09/08/2020
Divided tweets per languages and applied LDA on one batch. Probably there will be problem loading and preprocess the tweets in real time, but one thing every day.
I'll probably use REDIS for ingestion and 'waiting' on preprocess, then i'll upload the processed tweet on a mongodb cluster based on language.

### Sab. 08/08/2020
Applied LDA in order to get topics togheter, but there are bottlenecks:
  1. Languages -> need to figure out to 
  2. Preprocess -> more languages, more very specific preprocessing techniques
  3. Power -> my computer sucks and i dont want/dont need to optimize code also in a preliminary phase.
  
I need to ask if the analysis will be applied to simple english tweets or might be generalized to other languages: if so, i need a way to pass certain preprocess to a tweet based on lang, or maybe 'translate' everything in a lingua-franca: need to think on. 
The best way to me is to split the tweet based on the language, and sanity check the conditions (for example, number of tweets for every language), and from them apply all the preprocessing stopwords removal ecc needed.
Also probably I need to migrate on Google Colab since i don't want to wait 60+ minutes only to do the preprocessing (and also need to apply LDA).
  
### Ven. 07/08/2020
Created a TelegramBot in order to be updated on twitter stream: it has only one feature but can scale quickly, because its very easy to add things. I deployed on Heroku BUT since i dont want to open the connection to anyone on MongoDB cluster and Heroku server doesn't have a static IP, i cannot whitelist them and so the bot will work only when it will be updated in the uni computer. The rest of the day i'll try to create other features and stuff, then i'll read redis and i'm going to have a read on transformers.

### Gio. 06/08/2020
Solved every problems that i had yesterday, fixed the listener and finally get some tweets: i get 1.2M in few hours. Don't know if the number make sense, but i think that i lose some data during the way, both for connection errors and for sleep intervals. I finally did some analysis and the flux of tweets seems constant, but it can fetch only real time tweets and not past text, so this could be a strong limitation to our problem.
I also learnt the difference between RETWEET and REPLY: in the first case, you reply to a tweet, in the second one you retweet it (exactly as written). Lots of people retweet instead of simply reply, so well i have to re-download a lots of data in order to gain retweet information.
BTW the stream now seems to work, probably need to set up for longer run (24h+) and try to have fault tolerance on the mongosDB.

N.B: The cluster went **Out of Memory** after 5 hours of stream, with 1_460_368 tweets of size 471.24MB and indexes of 13.98MB.


### Mer. 05/08/2020
So my computer crashes following the updates of Windows 10 and i spent the entire morining fix it. Then the listener with only the valuable attributes of tweets doesn't want to start, so essentialy today is almost a dead day. Tried to save the date looking for a way to connect MongoDB and Elasticsearch so then i'll have a fast way to collect and manage tweet text in analysis mode. I'll try to get things work for the rest of the day, but it will probably took also tomorrow.
I'll consider the option to migrate on google colab if my computer won't work, using online resources until i'll have the access to the unimib computer.

### Mar. 04/08/2020
Run out of memory on MongoDB online, but for now it's enough.
I downloaded 82363 documents, with a total size of 511.54MB.
I need to consider to download only what i'll need for the analysis, so like attribute ["full-text","user","retweeted_from","lang","created_at"], so size might drop a lot.
In the meantime i used [Text-clean](https://github.com/jfilter/clean-text) for cleaning text based on language and i did a small script to load all documents text from Mongo.
Did the filter for all the relevant attributes, and get the text_extended when truncated field is equal to True: now each tweet is less informative 'but it's more lighter.
ATTRS = ["id","created_at","in_reply_to_user_id","in_reply_to_status_id","lang","text","user_id"]
- Every user is recognized based on ID and not on screenname or username (its literaly the same)
- Get bot user id and status id from retweet, because will be useful for stance detection. 
- I need to consider to add 'link' references, such as complete link that i might need to scrape them.

### Lun. 03/08/2020
Setting up the conda enviroment, updated all packages and created another cluster in MongoDB. It took all day, because my computer is commodity hardware and because there was problem with dns connecting to the mongoDB online cluster.

### Sab 01/08/2020 - Dom. 02/08/2020
Week end offline
