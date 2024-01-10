---
sidebar_position: 7
---

# Distributed Mutual Exclusion
mutual exclusion:
   is a concurrency control property to prevent processes from changing same thing simultaneously.


Mutual Exclusion in a single computer:
is achievable using a shared variable as all of the process would be sharing common memory. (semaphores).

But in distributed system, we neither have common memory nor synchronized physical clock, so we achieve mutual exclusion through passing messages.

token based approach:
a token is shared among processes by the leader node, process with token can only enter its critical section.

non token based approach:
processes communicate with each other  to decide entering the critical section sequence. they also need to maintain a logical clock to ensure resolving conflict.
example : ricart agarwala algo


quorum  based approach:

Instead of requesting permission for entering CS, a subset of processes called quorum's permission is required.
any 2 subsets must have a common process in them.

example is maekawa's algo
