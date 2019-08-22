---
layout: post
title:  "Serverless Data Analysis wih Google BigQuery and Cloud Dataflow"
date:   2019-08-21
desc: "Serverless Data Analysis on the Google Cloud Platform Introduction "
keywords: "Serverless, BigQuery, Dataflow, GCP"
categories: [GCP]
tags: [Jalpc,Jekyll]
icon: icon-html
---

Serverless Data Analysis allows organizations to carry out no-ops data warehousing using <b>BigQuery</b>, and pipeline processing using <b>Cloud Dataflow</b>. 

<b>Google BigQuery</b> is a data warehouse that you interact primarily through <b>SQL</b>, and <b>Cloud Dataflow</b> is a data processing pipeline system that you can program against in either <b>Python</b> or <b>Java</b>. 

Serverless Data Analysis is meant for people who build data pipelines and data analytics. It is imperative that an individual working with these tools have a solid understanding of SQL, because of interactions with BigQuery, and know either Python or Java, to work with Dataflow.

<h3>
<b>Deep Dive into BigQuery:</b><br />
</h3>
Why exactly is BigQuery? BigQuery is Google's no-ops solution to data warehousing and analytics systems, and by no-ops in this context essentially means that there is no infrastructure for you to manage, so no operations. It allows an individual to store data, analyze the data and export the data from a centralized location. In this post we will look at (1) how to do queries, (2) functions, (3) how to load and (4) export data. And we'll also look at some advanced features, like (5) nested and (6) repeated fields. (7) How to do window functions and (8) how to do user-defined functions.

1:44
And along the way, we'll do a few labs on queries and functions, on loading and exporting data and on demos. And I'll do a few demos.
1:56
Then we'll move on to talking about Cloud Dataflow, which is also no-ops in the sense that you don't need to manage any infrastructure. But here you're going to be writing programs that process data. And the kind of processing that you tend to do can either be on batch data or can be on streaming data and as we will see in data flow you get to write the exact same code, it works in both batch and stream. So if you need reliable, scalable data processing on GCP, the best option is Cloud Dataflow. So we look at data flow, we'll talk about what a data pipeline is. We will talk about how you can do math produce, which is the most common type of algorithms, big data algorithms that you might be doing today. We will look at how you would do those kinds of algorithms in data flow and with that, get the benefit that you can work with real time data, and historical data in exactly the same way. We will look at what are called side inputs. For the most part when your writing a data pipeline you'll have this one massive data set that you're processing as it comes in and you're writing things out. But usually, along with that big data set, you will have other smaller data that you need to get and join with. Those smaller data sets are called side inputs. So we will look at how to deal with side inputs in data flow. Then, we will also look at streaming, because again, one of the key advantages of data flow is the idea that you can process batch data and streaming data at the same way. So having looked at examples of use cases that use batch data we will then look at how to do streaming data and data flow. And the code itself would be very similar to the way you deal with batch, with a few extra concepts that come along because you're dealing with infinite data, unbounded data. So, in terms of labs, we will look at how to create a simple pipeline, how to write map produced jobs, how to incorporate side inputs, and along the way we'll also do some demos. A quick introduction to myself, my name is Valliappa Lakshamanan, everyone calls me Lak. I'm the professional services org of Google, I have a PhD in electrical engineering. I worked for a long time on weather research, so building data pipelines for doing real-time weather prediction and real-time weather diagnosis, so built a lot of machinery models for that. >> Hello, everyone. My name is Ajay Hemnani, and I'll be assisting Lak in this course. I'm a technical curriculum developer at Google, and I've worked on the Big Data and Machine Learning Fundamentals course as well as the other courses in the data engineering specialization. Lak and I will be joined by Tom in presenting this course. And so, Tom, please introduce yourself. >> Greetings. My name is Tom Stern. I'm another instructor and a technical curriculum developer at Google, and I'll be assisting Lak. I'm the author of Architecting Google Cloud Platform, Infrastructure and Architecting Google Cloud Platform, Design and Process. And have also been working on updates to courses in the data engineering specialization. Lak, please tell us some more about this course. >> My goal here is to talk to you about how you could deal with very large data sets, both from a declarative way with BigQuery and the programmatic with Dataflow. Such that you don't need to spin up any servers or manage any infrastructure. You can essentially write your logic, and your logic can be SQL statements, or they can be Python or Java programs. And you can get your logic executed on the cloud against massive data sets, small data sets, against data sets, and not have to manage infrastructure. It can be extremely liberating. As a data scientist and as a data engineer, if you can get to focus on your data, and the two key products on GCP that let you focus on your core logic and leave the infrastructure management to the cloud provider. The two key products are BigQuery and Dataflow, and that's what we're going to be looking at in this course. 

```
hello world
123
This is a text snippet
```


This is a JavaScript snippet:

```
const add = (a, b) => a + b
const minus = (a, b) => a - b

console.log(add(100,200))  // 300
console.log(minus(100,200))  // -100
```

This is a Python snippet:

```
def say_hello():
    print("hello world!")

say_hello()   // "hello world!"
```




