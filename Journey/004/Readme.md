
# AWS EC2

## Introduction

✍️ Amazon Elastic Compute Cloud, EC2 is a web service from Amazon that provides re-sizable compute services in the cloud.

## Prerequisite

✍️ SSH,
AWS account

## Use Case

- It is very difficult to predict how much computing power one might require for an application which you might have just launched. There can be two scenarios, you may over-estimate the requirement, and buy stacks of servers which will not be of any use, or you may under-estimate the usage, which will lead to the crashing of your application. 

## Cloud Research

Amazon Elastic Compute Cloud, EC2 is a web service from Amazon that provides re-sizable compute services in the cloud.

### How are they re-sizable?
They are re-sizable because you can quickly scale up or scale down the number of server instances you are using if your computing requirements change.


That brings us to our next question.

### What is an Instance?

An instance is a virtual server for running applications on Amazon’s EC2. It can also be understood like a tiny part of a larger computer, a tiny part which has its own Hard drive, network connection, OS etc. But it is actually all virtual. You can have multiple “tiny” computers on a single physical machine, and all these tiny machines are called Instances.

### Difference between a service and an Instance?

Let’s understand it this way:
EC2 is a service along with other Amazon Web Services like S3 etc.
When we use EC2 or any other service, we use it through an instance, e.g. t2.micro instance, in EC2 etc.


### Why AWS EC2?

Why not buy your own stack of servers and work 
independently? Because, suppose you are a developer, and since you want to work independently you buy some servers, you estimated the correct capacity, and the computing power is enough. Now, you have to look after the updation of security patches every day, you have to troubleshoot any problem which might occur at a back-end level in the servers and so on. These are all extra chores that you will be doing or maybe you will hire someone else to do these things for you.

But if you buy an EC2 instance, you don’t have to worry about any of these things as it will all be managed by Amazon; you just have to focus on your application. That too, at a fraction of a cost that you were incurring earlier! Isn’t that interesting?

### Let’s understand Cost Savings using an example.

Suppose instead of taking AWS EC2, we consider taking a dedicated set of servers, so, what all we might have to face:

. Now for using these servers, we have to hire an IT team which can handle them.

. Also, having a fault in the system is unavoidable, therefore we have to bear the cost of getting it fixed, and if you don’t want to compromise on your up-time you have to keep your systems redundant to other servers, which might become more expensive.

. Your own purchased assets will depreciate over the period of time, however, as a matter of fact, the cost of an instance have dropped more than 50% over a 3-year period, while improving processor type and speed. So eventually, moving to Cloud is all more suggested.

. For scaling up we have to add more servers, and if your application is new and you experience sudden traffic, scaling up that quickly might become a problem.


These are just a few problems and there are many other scenarios which make the case for EC2 stronger!


### Let’s understand the types of EC2 Computing Instances:


Computing is a very broad term, the nature of your task decides what kind of computing you need.
Therefore, AWS EC2 offers 5 types of instances which are as follows:

1. General Instances
For applications that require a balance of performance and cost.
E.g email responding systems, where you need a prompt response as well as it should be cost-effective since it doesn’t require much processing.
2. Compute Instances
For applications that require a lot of processing from the CPU.
E.g analysis of data from a stream of data, like a Twitter stream
3. Memory Instances
For applications that are heavy in nature, therefore, require a lot of RAM.
E.g when your system needs a lot of applications running in the background i.e multitasking.
4. Storage Instances
For applications that are huge in size or have a data set that occupies a lot of space.
E.g When your application is of huge size.
5. GPU Instances
For applications that require some heavy graphics rendering.
E.g 3D modeling etc.
Now, every instance type has a set of instances which are optimized for different workloads:
1. General Instances
t2
m4
m3
2. Compute Instances
c4
c3
3. Memory Instances
r3
x1
4. Storage Instances
i2
d2
5. GPU Instances
g2
Now let’s understand the kind of work that each instance is optimized for, in this AWS EC2 Tutorial.


### Burstable Performance Instances

T2 instances are burstable instances, meaning the CPU performs at a baseline, say 20% of its capability. When your application needs more than 20% of the performance of the CPU, the CPU enters into a burst mode giving the higher performance for a limited amount of time, therefore work happens faster.

You get these credits when your CPU is idle.

Each CPU credit gives a burst of 1 minute to the CPU.

If your CPU credits are not used they are credited to your account and they stay there for 24 hours.

Based on your credit balance, you can decide whether the t2 instance, should be scaled up or down

These bursts happen at a cost, every time a burst happens in a CPU, CPU credits are used.

### EBS-Optimized Instances

C4, M4, and D2 instances are EBS optimized by default, EBS means Elastic Block Storage, which is a storage option provided by AWS in which the IOPS* rate is quite high. Therefore, when an EBS volume is attached to an optimized instance, single-digit millisecond latencies can be achieved.
*IOPS (Input/Output Operations Per Second, pronounced eye-ops) is a performance measurement used to characterize computer storage devices.


### Cluster Networking Instances

X1, M4, C4, C3, I2, G2 and D2 instances support cluster networking. Instances launched into a common placement group are put in a logical group that provides high-bandwidth, low latency between all the instances in the group.

A placement group is basically a logical cluster where some select EC2 instances which are a part of that group can utilize up to 10Gbps for single flow and 20Gbps for multi-flow traffic in each direction.

Instances which are not a part of that group are limited to 5 Gbps speed in multi-flow traffic. Cluster Networking is ideal for high-performance analytics system.


### Dedicated Instances

They are the instances that run on single-tenant hardware dedicated to a single customer.
They are perfect for workloads where a corporate policy or industry regulation requires that your instance should be isolated from any other customer’s instance, therefore they go for their own separate machines, and their instances are isolated at the hardware level.
Let’s understand this through an example. Suppose in a company they have to follow the following tasks:


1. Analysis of customer’s data
Customer’s website activity, etc. should all be monitored in real-time. There will be times when the traffic on the website will be minimum, therefore using a very powerful processor should not be considered, since it will become expensive for the company because it will not be used for every hour of the day. Hence, for this task, we might take t2 instances because they give Burstable CPU performance i.e when the traffic will be more the CPU performance will be increased accordingly to meet the requirements.

2. Our auto-response emailing system
It should be quick, therefore we would require systems, where the response time is as short as possible. This could be achieved by using EBS optimized instances, as they offer high IOPS and hence, low latencies.

3. The search engine on our website
It should be able to sort the keywords and return relevant results, therefore we might have 2 servers for this. One is the database and the other server for processing the keywords. Therefore, the communication between these servers should be at the maximum possible rate. To achieve this, we can put them in a placement group and for that, we have to use Cluster Networking Instances.

4. Some processes in every organization are highly confidential
Because these processes give us an edge over other companies, no matter how secure the servers, maybe, some policies are still made to be sure. Therefore, we might use Dedicated Instances for these kinds of processes.
We now know about instances, let’s learn how to launch these instances?

### AWS EC2 Pricing

In this AWS EC2 Tutorial, let’s start with the free things first!
AWS EC2 free tier allows 750 hrs of t2.micro instance usage per month!
The free tier for EC2 is valid for 1 year from SignUp of your AWS account.


### There are basically 3 pricing options in EC2:

1. Spot Instances
2. On-Demand Instances
3. Reserved Instances

### Spot Instances

 is a pricing option which enables you to bid on unused EC2 instances. The hourly price for a Spot Instance is set by AWS EC2, and it fluctuates according to the availability of the instances in a specific Availability Zone.

Basically, you will set a price for an instance above which you do not wish to get charged for.

The price that you set is for per hour basis, therefore the moment the price for that instance becomes greater than what you have set, the instance gets shut down automatically.


### On-Demand Instances
 are used when you want to pay for the hour, with no long-term commitments and upfront payments. They are useful for applications that may have unpredictable workloads or for test applications that are being deployed for the first time.


### Reserved Instances 
provide you with significant discounts as compared to On-Demand Instances. With Reserved Instances you reserve instances for a specific period of time with three payment options:
No Upfront
Partial Upfront
Full Upfront

And two-term lengths:
One Year Term
Three Year Term
### The higher the upfront payment is, the more you save money.!!!



## Try yourself

✍️ Add a mini tutorial to encourage the reader to get started learning something new about the cloud.

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 3 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

## ☁️ Cloud Outcome

✍️ (Result) Describe your personal outcome, and lessons learned.

## Next Steps

✍️ Describe what you think you think you want to do next.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
