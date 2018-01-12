# Face-Detection Insight-DE-2018

## Facial Recognition at Scale for PEX


  PEX.com is an internet video analytics company. Pex aims to build the most advanced video & music analytics platform on the Internet.

## Background

With over 7 billion video/audio files indexed and classified, and over 1 exabyte of data processed, PEX aims to build useful insights to create a meaningful and actionable suite of analytics products. 

For this project, PEX wants to know when and how human faces appear in each video. This data will be used to enhance their dataset for analytics tools.

### Size of Dataset

50 TB of structured video, audio, and social media data, including links to media files, and associated metadata. 
  
Data will be provided either through access to Postgres tables, or http links, or access to Google Cloud storage buckets.

### Scope of Project : 
  1.  Build a scalable pipeline that processes the videos provided and computes video features such as intensities, labels, duration and other relevant metadata.
  2.  Determine the faces across all the video frames of each video using the appropriate facial detection algorithms.
  3. Design and define the schema to persist the computed data. 
  4. Provide access APIs to retrieve and possibly updated the persisted data.
  5. Extensions to this project would be to have a streaming algorithm to process videos in real-time.

## Technologies
  1.  Input Data Storage : Amazon S3, optionally Google Cloud Storage if data is initially provided through Google Cloud.
  2.  Processing Framework: Spark, possibly using Python/PySpark with OpenCV
  3.  Facial Detection on different platforms
      * OpenCV (for Postgres Files)
      * Amazon Rekognition APIs for Facial Detection (for files on S3) 
      * Google Cloud Video Intelligence(for Google Cloud Files)
  3. Meta Data Storage on HDFS/S3 (to decide, based on input sources)
  5. Kafka to support near real-time processing.

### Break down of technologies

Spark vs Map/Reduce 

```
Spark utilizes in-memory caching and optimized execution for fast performance. 
Supports general batch processing, streaming analytics, machine learning, graph databases, and ad hoc queries.
Map/Reduce : Map has to complete and persist before Reduce operations. Not friendly for adhoc queries.
```
Kafka vs Kinesis

```
Kafka requires configuration and setup. Kafka is percieved to achieve a higher throughput than Kinesis. Kafka has low latency as compared to Kinesis. 
Kinesis much easier to setup, with built-in support
```
## Algorithm

Add additional notes about how to deploy this on a live system

## References

* [Kafka vs. Kinesis](https://blog.insightdatascience.com/ingestion-comparison-kafka-vs-kinesis-4c7f5193a7cd) - Insight Alumni
* [Template](https://github.com/PurpleBooth) - **Billie Thompson**


## Authors

* **Krishnaprabha Chari** 



## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet : Markdown Cheatsheet







  
