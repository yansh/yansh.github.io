---
layout: post
title: "No Apps Are the Best Apps"
modified:
categories: articles
excerpt: "Future of apps is no apps"
tags: [Future, Apps]
share: true
comments: true
image:
  feature:
date: 2015-03-10 
---

I recently came across an [article](http://blog.intercom.io/the-end-of-apps-as-we-know-them/) by [Paul Adam](https://twitter.com/padday) of Intercom, titled "THE END OF APPS AS WE KNOW THEM”. I found it interesting and insightful. Paul describes the on going evolution of the app design from "destination" silos on our devices into what is rapidly becoming systems of interconnected components. 

In [another](http://blog.intercom.io/design-futures-1-creating-systems-not-products/), more in depth post, Paul writes:

> "Thinking about systems rather than destinations is critical but it is not how most designers think today. Systems comprised individual components that are connected. These connected components have relationships between them; they can change each other. They can be separated and reaggregated in different ways." 

First, little disclaimer to put this post in a context. [Max Ott](http://www.nicta.com.au/people/mott/) of [NICTA](http://www.nicta.com.au) and I, have been talking about the [Internet of Information](http://yansh.github.io/articles/moana/) for a few years now. We motivated our discussion by claiming that the current network service does not align well with how applications are built and used. 

In this post, using the context provided by Paul Adams' post, I would like to speculate on how an information-centric  Internet service abstraction can better support current and future trends in application development.

## Apps as Information  Containers


> "The primary design pattern here is cards. Critically it’s not cards as a simple interaction design pattern for an apps content, __but as containers for [information] that can come from any app.__"

First, let’s looks closely of what is actually underpinning this current evolution of apps into cards? To me, cards-oriented design pattern is emerging, almost, as a necessity. In the current fast paced world, we don’t have time to open an app, we want to consume and react to the information as soon as we received. It should contain only the important bits, come within easy to follow context and presented in easy to read UI. In other words, it  needs to matched (almost tailored) to our needs, device, location, even our mood and personality. This is becoming ever so relevant and true with the rapid emergence of Internet of (all) Things (IoT) type computing with dozens of systems, running multiple apps and all wanting to connect and communicate with each other. 

You might've noticed, I replaced the word "content" with "information" from the original quote because this ultimately what apps are handling. Applications today are all about information consumption and dissemination. Sure, Twitter wants you to  get it from its app, and Facebook doesn’t want you to “Like” your Google+ post (at the time of writing G+ still exist) but ultimately from the information consumption point of view it’s all just information. Furthermore, while _Cards_ are very intuitive abstraction for designers, to developers they probably resemble a type of database [Views](http://en.wikipedia.org/wiki/View_(SQL)) which capture a  subset of relevant to applications information.  


Paul seems to notice that as well: 

>  "In a world of many different screens and devices, content needs to be broken down into atomic units so that it can work agnostic of the screen size or technology platform. So Facebook is not a set of webpages, or screens in an app. It’s a system of __objects, and relationships between them__." 

Exactly! Objects and relationships! In fact, you can represent everything using the this type of structure. It is not new. It’s called graph! [Semantic Web community](http://www.w3.org/standards/semanticweb/) has been trying to tell people and open their eyes to it for years, looking for the “killer” app to convert everyone. 

Tim Berners Lee  has even wrote about it in [his blog](http://dig.csail.mit.edu/breadcrumbs/node/215) : 

>  "In the long term vision, thinking in terms of the graph rather than the web is critical to us making best use of the mobile web, the zoo of wildly differing devices which will give us access to the system."

So imagine an Internet as a global information repository. In this context, apps are just information containers querying for the information they need and exposing it to other apps when they want to.

### So what is missing? 

The next step is the evolution is making the above type applications easier and streamline the whole process.  There are mature standards, developed by the Semantic Web community, that enable to capture, query and reason over an information graph, however the underlying Internet architecture doesn’t know of their existence. Internet  was designed in the 70s with different goals in mind. Nobody envisioned the evolution of Interconnected computers networks into interconnected "everything". At the time, a couple of fundamental protocols were  enough to support all the application layer needed to operate. Although, this largely remains true today, as Internet still relies on the same network stack, most of the burdened is carried by the application layer, with custom software stacks on top of the network which allows the giants of today's Internet to provide the services they able to facilitate today. I think the following Figure  by [Geek&Poke](http://geekandpoke.typepad.com/geekandpoke/2012/03/thank-god-not-everything-is-software.html) depicts the resulting reality quiet nicely.

<figure>
<img src="/images/tgns.jpg" alt="image">
<figcaption><b>Figure: Thank god not everything is software.</b> </figcaption>
</figure>

We need a common information representation abstraction (language) at the architectural level to allow for interworking of information in systems. This, we believe, will pave the way for a smoother interoperation between applications. 


The concept of an application will turn inside out, exposing the guarded up until now information, while keeping the proprietary logic locked. Consequently, applications development paradigm will shift from building apps as information silos to have apps leverage existing information produced by other apps. As [Don Symes, et al.,](http://research.microsoft.com/apps/pubs/?id=173076) put it, already today most apps are no longer designed and developed in a vacuum. They integrate and operate on external sources of information. Apps are not just being producers of information, they are consuming it as well. As this trends continues the boundaries between individual applications will start to fade--the age of no apps. Well, we might still call them that, but these would they will very dynamic, easily customisable and amorphous units.

### Building future "Apps"

How would you implement these type of "apps" on top of such information-centric architecture? This in fact would be relatively straightforward; apps are constructed by issuing queries , which  pull information from multiple information sources into information (graph) container (remember views), which is specific to applications' logic. For example, a social network app (like Facebook) an query for all information published by a group of "Friends". You can of course refine it further (e.g., to specific time range) but more importantly you are not restricted just to your social network. Your query can span across multiple “silos”, such as sensor data, i.e., notify whenever my friend tweets something next to my geo-location. You essentially linked Twitter, Facebook and GPS information into one; what is left is to nicely visualize it. Applications on top of information-centric service abstraction are built to operate and process information and deliver out comes back to the common space.   Apps interact with other apps and produce results that more apps can use. This can be really powerfull. Think Unix's pipelines.


Just as Tim Berners Lee envisioned there will apps (he calls them agents) operating on structured data (objects and relationships), converting it to actionable information (basically something you can engage with). These apps will be able to subscribe (type of query) to parts of the information space.  

Joining a service will take on a different meaning. Unlike today, when in most cases you are implicitly forced into using a service, not because it is the best one for you but just because it is most popular. (I like G+ :) When you start looking at it from the information point of view Facebook, Google, LinkedIn, even email will be able to operate over the same pool of information, enhancing each others capabilities.

The developers are handed a much more powerful abstraction with which they can develop much more semantically-rich and enhanced apps, mashed up from others sources of information (apps) which decided to share it. For instance, you can choose to share your information with another app like Facebook which perhaps will offer a service such as specific graph search (e.g., find things that you and your friends like), similarly LinkedIn can provide you with possible professional opportunities  based on the information you share. If you trust these services you allow them to tap them into your information. The difference to how it is done today is two fold: you decide what to share, and with whom and the processed info is published back in and can be reutilised by other trusted services.

The user is the main beneficiary because his  device is gradually transforms from a container of independent apps into something much more powerful an "information repository". As the boundaries between application/service fade away, apps will become merely projections of that information onto the UX space, e.g., in form of cards, lists, circles --- add your favorite design trend here.




