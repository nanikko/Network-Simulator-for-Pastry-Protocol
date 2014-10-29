###Pastry, Overlay network for decentralized object location and routing

Implemented self-organizing and self-adaptive **Pastry** API, with dynamic network join and route methods, that can be used to provide services for implementing Distributed Hash tables, peer discovery in a peer-to-peer network, group communication, naming and global storage.

Project was implemented as per the specifications in the research paper [Pastry: Scalable, decentralized object location and routing for large-scale peer-to-peer systems](http://research.microsoft.com/en-us/um/people/antr/PAST/pastry.pdf)

In the project, a overlay network of peers was created based on GUID keys associated with each peer in the peer-2-peer system. These GUID keys are a result of a hash function, SHA-512 on some unique identity of a peer, say it IP address (In our case we Generated GUID's using a random function using time of creation). Using such an overlay network, Pastry API that was implemented, provides application level routing and object location in a system consisting of many of thousands of peers.

The project was tested for 100,000 nodes and the average hops for routing of message from a sender to receiver was O(log n).
