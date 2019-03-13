## Project 0: Getting started with CPN and CPN Tools

This project consists of a set of small exercises to become familiar with CPN models and CPN Tools. The figure number below refers to the figure numbers in the CPN book.

The documentation for using CPN Tools can be found here: http://cpntools.org/2018/01/16/documentation-2/

### Exercise 1: Interactive and Automatic Simulation

Consider the <a href="../models/chapter2/2-10NondeterministicProtocol.cpn">simple protocol</a> in Fig. 2.10.

Use the CPN simulator to perform some interactive and automatic simulations of the CPN model. This should include scenarious where packets (data and acknowledgments) are lost and where overtaking occurs</p>

### Exercise 2: Reception of Acknowledgements

Consider the <a href="../models/chapter2/2-10NondeterministicProtocol.cpn">simple protocol</a> in Fig. 2.10. When an acknowledgement is received by the sender, it updates the counter on NextSend according to the number contained in the acknowledgement. This implies that the counter on `NextSend` can be decreased when an "old" acknowledgement is received. Use the CPN simulator and interactive simulation to construct a scenario where this situation occurs.</p>

Modify the CPN model such that the counter on `NextSend` will never be decreased. Use simulation to validate the modified model. Hint: use an if-then-else expression on the arc from `ReceiveAck` to `NextSend` comparing the variables `n` and `k`.

### Exercise 3: Bounded Retransmission

Consider the <a href="../models/chapter2/2-10NondeterministicProtocol.cpn">simple protocol</a> in Fig. 2.10. The CPN model specifies no upper bound on the number of times that a data packet can be transmitted.

Modify the CPN model such there is a bound on the number of times that a packet can be retransmitted. Hint: augment the colour set (type) of the place `NextSend` such that the token on `NextSend` is a tuple (pair) specifying the sequence number of the data packet currently being sent, and use a *guard-expression* on the `SendPacket` to enforce the upper bound on the number of retransmissions.  

Use simulation to validate the modified model.

### Exercise 4: Producer-Consumer System

Consider a producer-consumer system containing:

* A set of Producers: `PROD = {P1, P2, ..., Pnp}`
* A set of Consumers: `CONS = {C1, C2, ... , Cnc}`
* A set of Data: `DATA = {D1, D2, ... , Dnd}`

Each producer alternates between producing data and sending data. Analogously, each consumer alternates between receiving data and consuming data. The data items are exchanged via a buffer and each data item goes from one producer to one consumer.

1. Make a CPN model of the producer/consumer system with 3 producers, 2 consumers and 4 different kinds of data. The three sets above can conveniently be modelled by means of <a href="http://cpntools.org/2018/01/09/index-color-sets/">index colour sets</a>. Make a simulation of the CPN model.

2. Modify the CPN model so that producers only can send data to consumers who have the same or a lower number. Make a simulation of the new CPN model.

### Exercise 5: Dining Philosophers System

Consider a system where a number of Chinese philosophers are situated around a circular table. In the middle of the table there is a delicious dish of rice, and between each pair of philosophers there is a single chopstick. Each philosopher alternates between thinking and eating. To eat, the philosopher needs two chopsticks, and he is only allowed to use the two which are situated next to him (on his left and right side). It is obvious that this restriction (lack of resources) prevents two neighbours from eating at the same time.</p>


1. Make a CPN model of the dining philosophers system with 5 philosophers. It is assumed that each philosopher simultaneously (and indivisibly) picks up his pair of chopsticks. Analogously, he puts them down in a single indivisible action. Make a simulation of the CPN model.

2. Modify the CPN model so that each philosopher first takes his right chopstick and next the left one. Analogously, he first puts down his left chopstick and next the right one. Make a simulation of the new CPN model. Does the modification change the overall behaviour of the system (e.g., with respect to deadlocks and fairness between the philosophers)?

3. Modify the CPN model, so that each philosopher takes the two chopsticks one at a time (but now in an arbitrary order, which may change from time to time). Analogously, he puts down the two chopsticks one at a time (in an arbitrary order). Make a simulation of the new CPN model. Does the modification change the overall behaviour of the system (e.g., with respect to deadlocks and fairness between the philosophers)?


### Exercise 6: Gas Station

Consider a gas station with a number of customers, three different pumps and one operator. When a customer arrives at the gas station he pays the operator. Then the operator activates the relevant pump. The customer pumps the desired quantity of gasoline (the maximum quantity is of course determined by the prepaid amount of money). Finally, the customer receives his change from the operator (if any).
