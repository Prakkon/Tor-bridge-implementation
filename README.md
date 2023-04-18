# Tor Bridge Implementation

### Implementation Process

- Create and run a cloud VM instance, create a Tor Network on the same. 
- Refer to the [Official Documentation](https://www.community.torproject.org) for the environment setup and bridge relay addition.
- Check out the [vmspecs.txt](vmspecs.txt  for the dependencies and minimum size, memory requirements to run the tor network.
- Create a torrc file for configuration management, add [config.txt](config.txt) in it (change it according to your requirements)
- use ``systemctl`` to ``enable``, and ``start`` your tor network.
- instantiate a tor bridge on the tor network.
- install the [nyx tool](nyx.torproject.org/#download)  and run it to monitor your tor bridge.
- install the libraries required to run the python visualizations
- transfer the ``cache.sqlite`` file generated by nyx tool in /root/.nyx directory to your local directory using ``scp`` command
- generate visualizations by running the ``blink.py`` script using ``cache.sqlite`` as an input.
---

### Working Procedure

- A user fires up the client and connects to the network through what’s called an entry node. 
- To reach a website anonymously, the user’s Internet traffic is then passed encrypted through a so-called middle relay and then an exit relay 
(and back again). 
- That user-relay connection is called a circuit. The website on the receiving end doesn’t know who is visiting, 
only that a faceless Tor user has connected.
---

### Tech Stack

Click to read the following:


<a href="cloud.google.com"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/googlecloud/googlecloud-original.svg" width="150" height="150" /> </a>
<a href="docs.python.org"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original-wordmark.svg" width="150" height="150" /> </a>
<a href="community.torproject.org"><img src="https://upload.wikimedia.org/wikipedia/commons/c/c9/Tor_Browser_icon.svg"  width="150" height="150" /> </a>
<a href="https://help.ubuntu.com/"> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ubuntu/ubuntu-plain-wordmark.svg"  width="150" height="150" /> </a>
<a href="https://go.dev/doc/"> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg" width="150" height="150" /> </a>

---

### Future Work

- check if two clients communicating with each other can access their ip info or not
- check how an enterprise can successfully implement this network architecture
- create a tor bridge for specifically Enterprise use-cases

---
