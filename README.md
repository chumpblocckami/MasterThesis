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
- [ ] ~~Kafka for stream acquisition~~ 
- [ ] ~~Kafka, MongoDB and TwitterListener in Docker on Azure
- [ ] ~~Jupyter/Spark in Docker on HDFS that load MongoDB (is that possible?)~~ might need
- [x] Working offline listener
- [ ] Master-Slave architecture for parallelize listeners and save them into the big database
- [ ] ElasticSearch on Lab-Server
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

### Literature and interesting stuff:

#### General:
- [NLP and Mental Health](https://www.researchgate.net/publication/313127241_Natural_language_processing_in_mental_health_applications_using_non-clinical_texts)
- [Learning to identify emotions in text](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.217.62&rep=rep1&type=pdf)
- [Assessing the Distributional Hypothesis in Word Bigrams](https://iris.unitn.it/retrieve/handle/11572/249655/297594/2019_how_much_competence_in_performance.pdf)

#### Conda:
-[Anaconda cheatsheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

#### Latent Dirichlet Allocation
- [Latent Dirichlet Allocation Andrew Y. Ng](http://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf)

#### Stance Detection:
- [Topical Stance Detection for Twitter: A Two-Phase LSTM Model Using Attention](https://arxiv.org/pdf/1801.03032.pdf)
- [Stance Detection in Web and Social Media: A Comparative Study](https://arxiv.org/pdf/2007.05976.pdf)
- [SOTA: stance detection](https://paperswithcode.com/sota/stance-detection-on-rumoureval)

##### Note:
- Carlo Strapparava è di Trento


That's all (**for now.**)
