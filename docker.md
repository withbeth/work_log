# Useful Commands

$ docker info
$ docker version
$ docker images
$ docker ps

# Book
# Ch1 : Introduction to Container-ization

## Diff between Container-ization and Virtualization
What Docker provides?
- Docker provides for OS level virtualization known as Containers. and its not
  same as HW virtualization.
What features of linex kernel Docker uses?
- Docker uses resources isolation features of Linux kernel such as
  cgroups(short for "controll groups",
  kernel namespaces, and so on.
- cgroups is Linux kernel features that limits and isolates resources usage(such
  as CPU, Memory, disk I/O and network) to a
  collection of processes.
What problems Docker solved?
1. Setting up dev's work env.
- Instead of tagetting OS and programming versions, targetting docker engine
  and the runtime.
2. Same issues on PROD env; what if we have to upgrade OS;
- Build a new container with the new app code and dependencies and ship it.
  Infras remains the same.
- Roll back plan : Re-deploying the older app container.
By having all the generated Docker images stored in Docker registry.
### Knowing the diff between Containers and Virtual Machines
What is the fundamental Diff?(Isolation level)
- Containers share the same kernel as host, which means kernel level isolation.
- Docker ONLY isolates a single process(or group of processes, depending on how
  the images is built) and all containers run on the same host OS system.
- In contrast, VM virtualizes an entier os system(from CPU to RAM to storage),
  which means not only do we need the app's dependencies, we also need an os
  system to run the application.


