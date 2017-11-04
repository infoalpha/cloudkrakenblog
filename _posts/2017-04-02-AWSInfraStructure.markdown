---
layout: post
title:  "AWS Infra Structure Basics"
date:   2017-04-02 11:34:20
categories: Cloud AWS
tags: AWS DataCenter EdgeLocation DirectConnect EndPoints TransitCenters
author: Cloud Kraken
image:
---

**AWS DATACENTER**

* A Datacenter is a location where actual physical data resides.
* Data center typically has 50000 to 80000 physical servers.
* A single or couple of data centers are clubbed in to one AZ.
* It’s hard to get how many datacenters Amazon operates, Below Map provided interesting map of AWS Data Centers

    http://www.turnkeylinux.org/blog/aws-datacenters.

**AWS Edge Location**

*	This is the location where content is cached to reduce latency between end user and geo location of hosted website.
*	An edge location is where end users access services hosted on AWS. 
*	This is separate from AWS Region/AZ.
*	Edge locations are not just read only. You can write objects to them (PUT). 200 ok will be received.
*	Objects are cached for the life of TTL.
*	We can clear objects before TTL expires but will be charged.
*	These are in most of the major cities around the world and are specifically used by Cloud Front (CDN) to distribute content to end user to reduce latency.
*	It is like frontend for the service we access which are in AWS cloud.


**AWS DIRECT CONNECT**


* An AWS direct connect is a service offered by Amazon for a dedicated optical fiber cable from your office premises to AWS cloud where you run your applications.
* Advantage of this service is :
    *   Provide adequate and dedicated bandwidth to your services located in AWS.
    *   To reduce latency from your network to AWS network.
    * Provide private connectivity to your services in AWS from your office network.

**AWS ENDPOINTS**

* An AWS endpoint is a URL used to access AWS web console.
* We Configure/use Aws Services using this URL.

**AWS TRANSIT CENTERS**

* A transit center is defined as a connection point between actual data center to customers.
* These transit centers are highly available connection centers which are independent of each other in a region.
* These are directly connected to all the available AZs in each region.

**Difference between AWS Endpoints and AWS Edge Locations**

* There is a relation between AWS endpoints and AWS edge location.
* AWS endpoints are used to connect to AWS web console service to configure AWS services such as EC2, S3 etc. by a company or engineers whereas AWS Edge location is where this service is served to the clients.

**What to know about physical location of AWS services/DC globally on a map? Then below map is for you.**

https://www.google.com/maps/d/viewer?msa=0&mid=z8tAG_iMI0RE.kBLn8p8h4GGw

<iframe src="https://www.google.com/maps/d/embed?mid=1m6v8XPxwp0Dx4THiakRKFkZwIGE" width="640" height="480"></iframe>



