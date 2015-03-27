---
layout: post
title: "FOG: close proximity, contextual related spaces "
modified:
categories: articles
excerpt:
tags: [draft, Fog]
image:
  feature:
date: 2015-03-10T10:35:56-04:00
---

Proposal for a Fog type use-case for a close proximity, decentralized cloud-service. The high level idea is about  looking at a scenario where (socially) connected users can leverage the storage at each others’ devices to form a close-proximity, contextual "cloud", e.g., home, street, office.

In a nutshell, the idea is to facilitate a virtual "cloud” type environment by abstracting the storage/computation on the near by devices. This is different from just sharing a folder in a "cloud", although might be presented to user as such. None of the participants actually stores the whole content and has control over the folder. The overall storage at the devices is determined by the collective portion of the authorized devices in the vicinity.


# Related work

Current approaches, use iCloud/Google/Dropbox drive to synchronised your files. This requires you to trust the third party provider to keep it secure. Second, an other extreme, completely decentrelised cloud, p2p approach, where storage is crowdsourced from a large number of users. There is an active project, [storj.io](http://storj.io), which requires strong incentive schemes to reach critical mass. 

Other approaches, including the one developed in Princeton, use third-party cloud for storage, however, employ secret sharing techniques to split content's chunks across the third party clouds. This stops the 3rd party from obtaining the whole content and reading it. The client on the  other hand can combine the chunks into a usable/readable content. Despite its privacy preserving benefits, this approach might suffer from performance issues, as request retrieval requires access to multiple clouds which have different delays associated with the connection.


# Fog alternative

As the edge becomes more powerful and the storage capabilities increase, it seem possible to design systems where users won’t require (or require less) to use the cloud for collaboration, storage or computation. 

The Fog networking presents an alternative approach, where clients can rely on the devices/AP in the nearby vicinity for storage and possibly computation. This is, however, inherently a distributed system and therefore needs to tackle very similar challenges posed by the [CAP](http://en.wikipedia.org/wiki/CAP_theorem) theory -- i.e., Consistency, Availability and (network) Failure. Reminder, it's proven that any system can only have any *two* of the three desired properties. 

As a distributed system, any fog type system, will require to state upfront what consistency, availability and (network) failure models does it support. The ultimate system will have to balance this trade-off between the  three properties,  i.e., so the consistency model will have an affect on the design choices for availability and (network) failure tolerance.

*Specific problem*  

> Mobile devices are overloaded with photos, require memory extension which often exist in a form of virtual space in the cloud. See Figure for illustration.

<figure>
<img src="{{ site.url }}/images/carboardbox.gif" alt="image">
<figcaption><b>SMH Cathy by Cathy Guisewite</b></figcaption>
</figure>

*Questions* 

Can a "home-cloud" be created?; where the photos are automatically offloaded to devices in family possession? As mentioned earlier, the context of home is just a use-case of what we can call "close proximity, contextual related space". Other spaces can be created as well, can and how will they interact? What is the radius needed to achieve critical mass -- family (num of people?), neighborhood (# houses)?



### A simple scenario -- photo album

A household of 2 kids + 2 adults can create a virtual “Home-cloud” to share memories within everyone in their home.
No need to upload it to the cloud. The home cloud comprises devices in the home's vicinity. We can assume a couple of static devices: TV setabox, private cloud and more dynamic devices such as smartphones, tablets, etc. These will come with corresponding characteristic and properties:

* A user with an iPhone (64G)
* Setabox TV - 1TB
* iPad 120GB
* Laptop
* A car? 




__Scanarios:__

* Everyone is at home.
* Everyone is away -- what happens to the home cloud?
* Part of the family is at home -- how that effects the service? does it break?
