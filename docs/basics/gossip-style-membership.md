---
sidebar_position: 5
---

# Gossip style membership


so as we know failures is a norm rather than the exception in data centers.
and we at all cost need to detect those failures and be aware.
In this case, Membership list comes into the picture which keeps the statuses of the processes based on their heartbeat count. If it does not receive heartbeat from any of the processes, it marks that process down and updates the member ship list and notify the centralized server which is the master authority of true member ship list. 

But centralized does uprise the SPOF (single point of failure) disadvantage by default, so guess we need something counter intuitive.
presenting you the problem solver
Gossip style Membership Protocol.

In this protocol each process randomly select n processes of the system and sends them a heartbeat. This will make them update their member ship list. In this way heartbeats get send all the time so the updation of membership list. If the heartbeat of any processes doesn't increase after threshold time, that process will be marked inactive.

TC: O(N log(N)) time