---
layout: post
title:  "Introduction to Serverless Data Analysis with Google BigQuery and Cloud Dataflow"
date:   2019-08-21
desc: "Serverless Data Analysis on the Google Cloud Platform Introduction "
keywords: "Serverless, BigQuery, Dataflow, GCP"
categories: [GCP]
tags: [Jalpc,Jekyll]
icon: icon-html
---

Serverless Data Analysis allows organizations to carry out no-ops data warehousing using <b>BigQuery</b>, and pipeline processing using <b>Cloud Dataflow</b>. 

Google BigQuery is a petabyte scale data warehouse on Google Cloud that you interact primarily through <b>SQL</b>, and Cloud Dataflow is a data processing pipeline system that you can program against in either <b>Python</b> or <b>Java</b>. 

Serverless Data Analysis is meant for people who build data pipelines and data analytics. It is imperative that an individual working with these tools have a solid understanding of SQL, because of interactions with BigQuery, and know either Python or Java, to work with Dataflow.
<h3>
<b>What is BigQuery?</b>
</h3>
BigQuery is Google's no-ops solution to data warehousing and analytics systems, and by no-ops in this context essentially means that there is no infrastructure for you to manage, so no operations. It allows an individual to store data, analyze the data and export the data from a centralized location. 
<h4>
<b>BigQuery offers:</b>
</h4>
<ul>
  <li>Interactive analysis of petabyte scale databases. </li>
  <li>Familiar, SQL 2011 query language and functions.</li>
  <li>Many ways to ingest, transform, load, export data to/from BigQuery.</li>
  <li>Nested and repeated fields, user-defined functions in JavaScript.</li>
  <li>Data storage is inexpensive; queries charged on amount of data processed.</li>
</ul>
<h4>
<b>Benefits of BigQuery:</b>
</h4>
<ul>
  <li>BigQuery separates out storage and compute. </li>
  <li>Near-real time analysis of massive datasets.</li>
  <li>No-ops; Pay for use.</li>
  <li>Durable (replicated), inexpensive storage.</li>
  <li>Immutable audit logs.</li>
  <li>Mashing up different datasets to derive insights.</li>
</ul>
<h3>
<b>What is Dataflow?</b>
</h3>
Dataflow is a way by which you can execute <b>Apache Beam</b> data processing pipelines on the cloud.  It does so in a series of steps, and the key thing about Dataflow is that these steps called transforms can be elastically scaled. The code that is written is in an open source API called <b>Apache Beama</b>, and Dataflow is not the only place that you can execute Apache Beam pipelines, you can execute them on <b>Flink</b> or <b>Spark</b> etc, but Cloud Dataflow is usually used as the execution service for when we have a data pipeline that we would like to execute on the cloud. 
<b>What is Apache Beam?</b>
</h3>
Apache Beam is an open source, unified model for defining both batch and streaming data-parallel processing pipelines. Using one of the open source Beam SDKs, you build a program that defines the pipeline. The pipeline is then executed by one of Beam’s supported distributed processing back-ends, which include <b>Apache Apex</b>, <b>Apache Flink</b>, <b>Apache Spark</b>, and <b>Google Cloud Dataflow</b>.


   
   
                   


