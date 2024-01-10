---
sidebar_position: 3
---

# gossip algorithm
<!-- 
Docusaurus creates a **page for each blog post**, but also a **blog index page**, a **tag system**, an **RSS** feed...

## Create your first Post

Create a file at `blog/2021-02-28-greetings.md`:

```md title="blog/2021-02-28-greetings.md"
---
slug: greetings
title: Greetings!
authors:
  - name: Joel Marcey
    title: Co-creator of Docusaurus 1
    url: https://github.com/JoelMarcey
    image_url: https://github.com/JoelMarcey.png
  - name: Sébastien Lorber
    title: Docusaurus maintainer
    url: https://sebastienlorber.com
    image_url: https://github.com/slorber.png
tags: [greetings]
---

Congratulations, you have made your first post!

Feel free to play around and edit this post as much you like.
```

A new blog post is now available at [http://localhost:3000/blog/greetings](http://localhost:3000/blog/greetings). -->
gossip based algorithm falls  under AP which signifies high availability similar to under the hood operations of cassandra database.

the purposes of centrally controlled system or peer to peer decentralized system are as follows
system state = knowledge of other nodes in the system mostly their liveness status
communication = between processes


so basically in gossip based system, processes exchange statuses of each other and of other processes they know about time to time.

it is considered to be highly scalable and robust as it firmly backs eventual consistent membership list and obv fault detection and even can piggy back other info along with gossip messages and spread that around the whole network

+
so in a cluster of processes, each one of them maintains a list of known members and their address and maybe some meta data. Periodically each member using heartbeats updates the list of members and share with its known neighbors members.

on receiving gossip message from neighbors, each member merges the list in the message with its own list and adopts the max heartbeat counter for the receiving members. Processes determine the health of any process by their heartbeat count, if the heartbeat counts is increasing the process is considered healthy otherwise its not if hasn't increased for a defined threshold time.