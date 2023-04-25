# Tor Bridge Implementation

### Introduction

The very idea came up as a potential solution to a very common problem that exists in the current society- Privacy and Identity theft. From being stalked online to big MNCs stealing your information and selling it off for their ad revenue to getting threatened in real life over having an opinion. There's a lot of ways other people can use your digital footprint to cause harm to you physically and emotionally. Sometimes, such damage is irreversible and fatal.

Whistleblowers have to live in fear for theirs and their families' lives for having the courage to speak up. Journalists can't present information without getting half their material censored. Parents have to live with the fact that some psychopathic pedophile might know the school their kids go to, what neighborhood they live in, what time they go swimming. But hey, at least Facebook has some ads on what swisuits to buy. What a life saver!

It is, however, a moral dilemma to implement a network that keeps your identity truly anonymous. 
Such a network empowers users who wish to abuse the lack of accountability for their actions. They have no authority to fear, therefore they are free to cause misinformation, distress and even riots on communal grounds. 

What would you do with such a network? Well while you ponder, here's how to build one!

### Let's get started

- Create and run a cloud VM instance, create a Tor Network on the same. 
- Refer to the [Official Documentation](https://www.community.torproject.org) for the environment setup and bridge relay addition.
- Check out the [vmspecs.txt](vmspecs.txt) for the dependencies and minimum size, memory requirements to run the tor network.
- Create a torrc file for configuration management, add [config.txt](config.txt) in it (change it according to your requirements)
- use ``systemctl`` command to ``enable``, and ``start`` your tor network.
- instantiate a tor bridge on the tor network.
- install the [nyx tool](nyx.torproject.org/#download)  and run it to monitor your tor bridge.
- install the libraries required to run the python visualizations
- transfer the ``cache.sqlite`` file generated by nyx tool in /root/.nyx directory to your local directory using ``scp`` command
- generate visualizations by running the ``blink.py`` script using ``cache.sqlite`` as an input.

NOTE: If this doesn't help, try referring to [The research doc](Tor%20ridge%20Implementation.pdf)

---

### How does TOR Network work?

- A user fires up the client and connects to the network through what’s called an entry node. 
- To reach a website anonymously, the user’s Internet traffic is then passed encrypted through a so-called middle relay and then an exit relay 
(and back again). 
- That user-relay connection is called a circuit. The website on the receiving end doesn’t know who is visiting, 
only that a faceless Tor user has connected.
---

### Tech Stack

Click to access the documentation for the following:


<a href="cloud.google.com"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/googlecloud/googlecloud-original.svg" width="150" height="150" /> </a>
<a href="docs.python.org"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original-wordmark.svg" width="150" height="150" /> </a>
<a href="community.torproject.org"><img src="https://upload.wikimedia.org/wikipedia/commons/c/c9/Tor_Browser_icon.svg"  width="150" height="150" /> </a>
<a href="https://help.ubuntu.com/"> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ubuntu/ubuntu-plain-wordmark.svg"  width="150" height="150" /> </a>
<a href="https://go.dev/doc/"> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg" width="150" height="150" /> </a>

---

### Conclusion

So is it worth it? What you made is an isolated network with live information of users accessing the internet via tor bridges. You could, in fact, create a tor bridge-relay network isolated for your religious cult or terrorist organization. Or you could make one to bring such organizations to light. 
There are multiple steps implemented to stop users from abusing the tor network entirely. as the tor relay database encrypts your ip as constantly changing public domain... but it doesn't make it vanish. Or change it, entirely. It hides your digital footprint, and can be accessed by the peer network admin.
For example, The FBI recently closed a criminal case against the owner of Freedom Hosting, a dark web service that ran on the Tor network.

In addition, several research projects have shown varying levels of successful attacks that either attempted to eavesdrop on Tor-encrypted traffic or identify users.
Well that is where tor bridges can successfully revive the old career of TOR Networks where they used to be a thorn in law enforcement.

---

### Future Work

- check if two clients communicating with each other can access their ip info or not
- check how an enterprise can successfully implement this network architecture
- create a tor bridge for specifically Enterprise use-cases
- create checkpoints within the network to stop promoting inflamatory content, misinformation

---
