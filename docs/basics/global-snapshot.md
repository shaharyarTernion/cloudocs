---
sidebar_position: 6
---

# Global Snaphshot
Global Snapshot or state consists of local states of each process and their channel states.

 Snapshot Problem:
Grasping the total state of the system without stopping it.

Global Snapshot can be used to
. finding the load on the distributed system.
. finding if there's any deadlock
. for garbage collection

2 of the major problems in global snapshot is 
1) You cant catch all the process at a time.
2) You cant see the messages in the channel states.


Chandy Lamport Global Snapshot Algorithm.
system state:
channels and processes are reliable, dont fail.
processes capture their local states and incoming channel state
channels are unidirectional and provide FIFO order delivery
any process can initiate Global Snapshot Algorithm
the algorithm must not interfere with the other tasks of the process



 The algorithm has three phases: Initiation, Propagation and Termination and works as follows:
First is Initialization:

Initiate GSA, The Process Pi capture its local state, then create and send marker messages to all other processes using (N-1) outbound channels Cij(j = 1 to N & j != i)  , then start listening to those incoming channels to record incoming messages.


Second is Propagation:
Process Pj receives the marker message at channel Ckj.
if this is first marker message it receives
. It captures its own state and then mark Ckj as empty, then send marker messges to all processes using N-1 outbound channels
and then starts recording messges on incoming channels Clj ( l is not equal to j or k)
if it has already received the marker message then 
just mark the state of the channel Ckj


Third is termination:

All of the process have received the marker messages. (process state has been recorded)

All of the processes have received maker messages on all N-1 incoming channels ( channel states have been recorded)

Now the central server can collect these partials state to create a global image.

Cut:
cut is a line slicing the space-time diagram line of the process in PAst and future section.

consistent cut:
consistent cuts represents a snapshot of the distributed state of the system at a particular point in time.
It obeys the causality of the events. (means event happened in the past can be initiated in the past and received in the future cut, be initiated and completed in the past, but cannot be initiated in the future and received in the past).
 
