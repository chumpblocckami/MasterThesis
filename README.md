## MasterThesis blog


# Detect psychological impact of covid-19 through user generated small texts

## TO DO LIST:
### 0. Beginning (18/07/2020 - 01/08/2020)
[*BLOG*](July.md)

- [x] How pages works, know the syntax, try to understand how add pages
- [x] Read some literature about detect mental state using NLP 
- [x] GANTT and understand how much time for every step

### 1. Data Managment (01/08/2020 - 01/09/2020)
[*BLOG*](August.md)
- [x] Working offline listener
- [x] Redis stream for data ingestion
- [x] Redis Subscriber
- [x] Redis Consumer
- [x] Filter on metadata
- [ ] Telegram Updates **fancy**

**FINAL GOAL: FAST, RELIABLE, USABLE DATABASE THAT AUTOMATIC UPDATES ITSELF USING THE STREAM**
### 2. Data Analysis (01/09/2020 - 01/11/2020)
- [ ] Spark 
- [ ] Keras/*Theano* in Spark
- [ ] Community detection
- [ ] Sentiment Analysis
- [ ] Other models for mental state detection
- [ ] Optimization

### 3. Presentation (01/01/2021 - )
- [ ] What and How present everything
- [ ] Flask app dashboard

### (H)Acknowledgments:
- [Kafka Documentation](https://kafka.apache.org/documentation)
- [Elastic Search Python Driver](https://elasticsearch-py.readthedocs.io/en/master/)
- [Redis](https://redis.io/)
- [Telegram bot on heroku](https://towardsdatascience.com/how-to-deploy-a-telegram-bot-using-heroku-for-free-9436f89575d2)
- [pyRedis](https://realpython.com/python-redis/#using-key-expiry)
### Literature and interesting stuff:

#### General:
- [NLP and Mental Health](https://www.researchgate.net/publication/313127241_Natural_language_processing_in_mental_health_applications_using_non-clinical_texts)
- [Learning to identify emotions in text](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.217.62&rep=rep1&type=pdf)
- [Assessing the Distributional Hypothesis in Word Bigrams](https://iris.unitn.it/retrieve/handle/11572/249655/297594/2019_how_much_competence_in_performance.pdf)
- [Moral information metrics from textual data](https://github.com/medianeuroscience/emfdscore)
- [Flair: State of the art NLP](https://github.com/flairNLP/flair)

#### Conda:
- [Anaconda cheatsheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

#### Latent Dirichlet Allocation
- [Latent Dirichlet Allocation Andrew Y. Ng](http://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf)

#### Stance Detection:
- [Topical Stance Detection for Twitter: A Two-Phase LSTM Model Using Attention](https://arxiv.org/pdf/1801.03032.pdf)
- [Stance Detection in Web and Social Media: A Comparative Study](https://arxiv.org/pdf/2007.05976.pdf)
- [SOTA: stance detection](https://paperswithcode.com/sota/stance-detection-on-rumoureval)

##### Note:
- Attended [AI for people workshop](https://github.com/aiforpeople-git/First-AI4People-Workshop), really insightful


That's all (**for now.**)
