---
sidebar_position: 9
---

# Transactions + 2PC
a unit of task performed in a database.

but when you have multiple servers of a database you can look for distributed transactions. 

two phase commit is one of the common distributed transactions algorithms.

As the name suggests its divided into 2 phases, first one is locking phase and the second one is commit phase.

working principle revolves around distributing locks against distributed processes so they can lock their local resources while committing happens .

