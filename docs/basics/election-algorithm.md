---
sidebar_position: 4
---

# Election Algorithm


Its motive is to elect a process which will serve as a coordinator or leader of all the processes.

1. The bully algorithm:
In this algorithm , active process which has the highest id gets elected as the leader.

Process P broadcasts an election message with its ID, on receiving
. if the process's id is higher than it will initiate an election message with its own ID.
. if the process's id is lower than its own than it sends back the Answer message

Network bandwidth for worst case is O(N^2).

2. The Ring Algorithm :
In this algorithm, the processes works as if they are formulated a ring. and sends message to the process next to it clockwise. 
On receiving election message from Process P, 
if the id is higher than its own id than it forwards the election message to the next process in the ring otherwise it append its own id in the election message and then forwards it .

When a process receives an election message with its own id, it announces victory by sending a victory message, (which circulates in the same manner). 

bandwidth wrt worst case:
0(N-1) . 0(N-1)