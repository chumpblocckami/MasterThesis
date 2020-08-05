### Mer. 05.08.2020
So my computer crashes following the updates of Windows 10 and i spent the entire morining fix it. Then the listener with only the valuable attributes of tweets doesn't want to start, so essentialy today is almost a dead day. Tried to save the date looking for a way to connect MongoDB and Elasticsearch so then i'll have a fast way to collect and manage tweet text in analysis mode. I'll try to get things work for the rest of the day, but it will probably took also tomorrow.
I'll consider the option to migrate on google colab if my computer won't work, using online resources until i'll have the access to the unimib computer.

### Mar. 04.08.2020
Run out of memory on MongoDB online, but for now it's enough.
I downloaded 82363 documents, with a total size of 511.54MB.
I need to consider to download only what i'll need for the analysis, so like attribute ["full-text","user","retweeted_from","lang","created_at"], so size might drop a lot.
In the meantime i used [Text-clean](https://github.com/jfilter/clean-text) for cleaning text based on language and i did a small script to load all documents text from Mongo.
Did the filter for all the relevant attributes, and get the text_extended when truncated field is equal to True: now each tweet is less informative 'but it's more lighter.
ATTRS = ["id","created_at","in_reply_to_user_id","in_reply_to_status_id","lang","text","user_id"]
- Every user is recognized based on ID and not on screenname or username (its literaly the same)
- Get bot user id and status id from retweet, because will be useful for stance detection. 
- I need to consider to add 'link' references, such as complete link that i might need to scrape them.

### Lun. 03.08.2020
Setting up the conda enviroment, updated all packages and created another cluster in MongoDB. It took all day, because my computer is commodity hardware and because there was problem with dns connecting to the mongoDB online cluster.

### Sab 01.08.2020 - Dom. 02.08.2020
Week end offline
