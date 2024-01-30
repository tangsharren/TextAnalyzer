In this project, several softwares are used including Kafka, Hadoop, Hadoop Distributed File System (HDFS), HBase, and Hive.
Watsons Malaysia's Instagram posts is scraped using the PhantomBuster website and stored in Hadoop Distributed File System (HDFS). From there, a Kafka producer is employed within the Hadoop environment to ingest and send this dataset to a Kafka topic called "watsons-topic."

A Kafka consumer is used to subscribe to the "watsons-topic" and process the messages within it. This process involves several essential transformations, including lowercasing, URL, number, emoji, punctuation, extra whitespace, and new line character removal, handling null value ensuring the data is clean and ready for analysis.

The refined dataset is then stored in HBase, a NoSQL database as a HBase table. 

The HBase table is retrieved for further preprocessing using the NLP tool: Lemmatizer & Contraction Handler with POS tagger. 
Lemmatization with part-of-speech (POS) tagging is an important preprocessing step for topic modeling on Instagram posts from Watsons Malaysia
Lemmatized text data can lead to better topic modeling results, as it reduces the dimensionality of the text data

The lemmatized text data is stored in HDFS and retrieved using Spark tools. Finally, text analytics including TF-IDF and topic modeling are performed.
