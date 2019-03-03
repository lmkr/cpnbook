
## Project 1: CPN Modelling

The project is concerned with CPN modelling and the aim is to make a number of modifications and extensions to the <a href="../models/chapter2/2-10NondeterministicProtocol.cpn">CPN model</a> of the simple protocol described in Chapter 2.</p>

### Task 1: Packet Generation

The initial marking of the place PacketToSend specifies six packets that are to be transmitted by the protocol.  When modelling the sliding window protocols in task 2 and 3, more packets will be required to explore the models.</p>

Modify the CPN model of the simple protocol such that there is a transition that adds a packet to PacketToSend whenever it occurs. The i'th packet should be given sequence number `i` and the data content `"i "`. The latter makes it easy to check that the packets are delivered in the correct order by the receiver.</p>

### Task 2: Go-Back-N Window Protocol

The simple protocol is a stop-and-wait protocol: The sender keeps sending the same packet until the matching acknowledgement is received. In <i>sliding window protocols</i>, it is possible for the sender to transmit several packets to the receiver before receiving an acknowledgement, i.e., the sender has a *sender window* containing *w* data packets which is currently under transmission and for which acknowledgement have not yet been received.

Modify the CPN model such that it models a Go-Back-N Window Protocol. In a Go-Back-N protocol, the sender sends all data packets in the current window and then wait for acknowledgements. If no acknowledgement is received (within a certain amount of time), the data packets in the window are all retransmitted. It should only be necessary to modify the Sender part of the CPN model.

Use simulation to validate the correctness of the protocol.

### Task 3: Selective Repeat Window Protocol

The Go-Back-N Window Protocol introduces the concept of a *sender window.* The basic idea of the Selective Repeat Window Protocol is that there is also a <i>receiver window</i> that allows the receiver to buffer packets received out-of-order. Furthermore, the receiver can explicitly request retransmission of a "missing" packet from the receiver by sending a *negative acknowledgement*.

Modify the CPN model such that it specifies a Selective Repeat Window Protocol.

Use simulation to validate the correctness of the protocol.
