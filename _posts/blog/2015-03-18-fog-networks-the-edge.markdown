---
layout: post
title: "FOG Networks @ the EDGE " 
modified:
categories: blog
excerpt: "A personal roadmap draft"
tags: [FOG, networks, EDGE lab, Princeton]
share: true
comments: true
image:
  feature:
date: 2015-03-18

---

I recently joined the [EDGE lab](http://scenic.princeton.edu) at Princeton University to work on the FOG networks. 

#Fog

The Fog networking paradigm is rapidly gaining momentum and maturity in both industry and academia. At this stage, Fog is a broad umbrella term which looks at exploring how the increase in storage and computational capacity at the edge devices can be leveraged to perform a range of functionalities which today are done in centralised manner (typically relying on some type of cloud technology). It covers many areas of research such as wireless networks, distributed computing, analytics and cognitive computing.
There is a lot of overlap with what Fog initiative seems to propose and the IoT agenda. So, to me, Fog is as an IoT substrate, alongside cloud and other type of existing technologies in areas of storage, networking and sensors.


## High-level research directions

At this stage, my focus is on the following research directions:

* Service abstraction for FOG-type services and tasks    
    * Provide a level of service abstraction for a mixture of technologies, enable virtualisation of resources for the ad-hoc, distributed and interconnected devices.
        * Investigate how information from multiple devices (end points) can be represented,
queried and acted upon
        * what (and how) functionality should be expose to the service
* Secure and privacy preserving information communication and storage.
    * Leverage the decentralised and distributed nature of Fog networks to provide a secure and privacy preserving computation and information storage.

The goal is to narrow it down to a concrete and interesting problem which while dealing with particular case will showcase the benefits of overall Fog approach.

# Use cases

My aim is to leverage some of the existing work carried out in the Edge lab and see how it can be applicable in a Fog-type networking scenario. 

##  "Close proximity, contextually related space"

Proposal for a Fog type use-case for a close proximity, decentralized "cloud"-type abstraction for storage, computation and configuration.
The high level idea is to look at a scenario where socially connected users can leverage storage at each others’ devices to form a close-proximity, contextual type "cloud".

### Homenets

Home environment presents an interesting opportunity for the Fog networking use-case. A typical home is a trustworthy ecosystem containing all the key elements of a fog network setup, namely different users, mobile (smart phones, tablets) and stationary devices (set top boxes, TVs and other smart appliances) that operate on heterogeneous networks.
It would be interesting to explore the benefits a Fog network in such environment which is on one hand fully representative of a typical fog scenario while on the other hand poses last restrictions on the privacy/security of the provided service. We of course will have to assume that the family members trust and won’t use malicious techniques to undermine each other.

## Information privacy

Gradually end users become more aware and concerned with their own personal data. The current cloud-based solution although provide a very convenient way for users to store their data, are facing some interesting challenges in term of guaranteeing privacy. Fog networks can emerge as a possible solution to the problem by allowing users to seamlessly store their data across their multiple devices without relying to a large extent on a centralised entity. Personal clouds are currently being examined by many research communities and fog networks can serve as a key substrate in the overall system design.

#Edge-lab related activities

The Edge lab is in a good position to tackle the core challenges behind Fog networks.

###Wireless networks

Much of the communication in Fog network will be facilitated over wireless networks. It would be interesting to see how the overall throughput and performance can be optimised for different tasks and services on top of Fog networks.

### HetNets

This work is relevant to Fog, in particularly, the algorithm for choosing the right/ultimate (based on a particular metric) interface for devices to communicate with each other. One possible application might be  delegating some work for a particular interface, e.g., download movies to WiFi. In a more complex case, abstracting the communication interface altogether.

### Smart Data Pricing

One of the main arguments for adopting Fog networks is that offloading some of the computation and storage to the edge can facilitate for a cheaper option. The related works so far have looked into a single user-device use-case, it would be interesting to look at how interconnectivity and resource sharing can offer a more economically preferable/competitive option to the currently available services which heavily rely on the cloud connectivity.

### Distributed (secure) storage 

The Fog network can act as distributed personal storage. The Edge lab developed CYRUS system that uses secret sharing for secure storing of content using 3rd party (public) storage providers. Although, Fog is shifting the paradigm from the cloud closers to the edge, secret sharing techniques can be used to distribute content across the close by devices. This can also serve as a hook for my [previous work on personal information storage at the University of Cambridge](http://yansnotes.blogspot.com/2015/01/work-summary-ocaml-labs.html). More on that soon.
