# Tor Bridge Implementation

### Process

- Create and run a cloud VM instance, create a Tor Network on the same. Refer to the [Official Documentation](https://www.community.torproject.org) for the same.
- Check out the [vmspecs.txt](vmspecs.txt) for the dependencies and minimum size, memory requirements to run the tor network.
- instantiate a tor bridge on the tor network.
- create a configuration file depending on the system requirements.
- install the [nyx tool](nyx.torproject.org/#download)  
- install the libraries required to run the python visualizations

Under Construction 🚧

---

### Working Procedure

- A user fires up the client and connects to the network through what’s called an entry node. 
- To reach a website anonymously, the user’s Internet traffic is then passed encrypted through a so-called middle relay and then an exit relay 
(and back again). 
- That user-relay connection is called a circuit. The website on the receiving end doesn’t know who is visiting, 
only that a faceless Tor user has connected.
---

### Tech Stack

Under Construction 🚧

---

### Future Work

- check if two clients communicating with each other can access their ip info or not
- check how an enterprise can successfully implement this network architecture
- create a tor bridge for specifically Enterprise use-cases

---
