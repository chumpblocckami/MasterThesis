### Mer. 29/07/2020
- Without the actual server i can't do much. The stream listener works and it saves everything on MongoDB: i checked the stream on every partition and it seems costant. Also [THIS](https://www.youtube.com/watch?v=pt8VYOfr8To) don't help.

### Mar. 28/07/2020
- We probably don't need to create and implement Kafka for this kind of project: the stream can be ingested using requests and manage the connections. For now i can be able to download 50k tweets in an online mongoDB. Then i need to analyze the tweet in order to gain information about when they are loaded: i think that are in real time. Then i need to decide if i want the texts or the tweets in an elasticsearch server.

### Lun. 27/07/2020
- Did the first Listener to the stream use simply a http get, everything saved in a mongoDB database. Then in the evening i'll do a quick analysis on the tweet.

### Ven. 24/07/2020 - Dom. 26/07/2020
- [WELL](https://www.youtube.com/watch?v=HL1UzIK-flA)

### Gio. 23/07/2020
- Talked with prof. I need to set up VM for tweet collection, and try to have a preliminary analysis on texts. What i need to check is : tweet date, tweet language and metadata. I can use whatever, so probably i'll use simple TwitterHandler class updated to my needs.

### Lun. 20/07/2020 - Mer. 23/07/2020
- Damn work.

#### Dom. 19/07/2020
- Kafka documentation: [Getting Started](https://kafka.apache.org/)
- Read [PAPER](https://iris.unitn.it/retrieve/handle/11572/249655/297594/2019_how_much_competence_in_performance.pdf) : is about the distributional hypothesis in bigrams (how Distributional Semantics is affected by data and how much is affected by the 'architecture' used). It also clearly sum up the golden approaches (the cited 'architecture') to NLP rappresentation.

#### Sab. 18/07/2020
- Added Github Pages
- Writed to prof. Viviani about Thesis Proposal
