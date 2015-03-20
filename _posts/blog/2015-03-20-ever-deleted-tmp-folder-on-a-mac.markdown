---
layout: post
title: "Ever Deleted /tmp Folder on a Mac?"
modified:
categories: blog
excerpt: "I have, here is how to bring it back!"
tags: [Tip, Mac]
image:
  feature:
date: 2015-03-20T11:40:34-04:00
---

```/tmp``` folder is used by the Mac OS apps to store temporary data. Any a week old content in the folder is earsed as well as every time you restart your machine. I accidently deleted it. Not a big deal, but any app that writes into will throw an exception. 

Creating a tmp folder, using ```mkdir``` doesn't help because ```tmp``` is not a folder it's a symbolic link to /private/tmp folder. 

Therefore to restore it you need to create the symbolic link again:

```
ln -s /private/tmp/ /tmp
```

That's it. Hope it helps!




