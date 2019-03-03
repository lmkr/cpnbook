## Project 2 : CPN State Space Analysis

The project is concerned with state space analysis and the goal is to apply full state spaces for verifying two variants of the simple protocol from Chapter 7.

The project consists of two tasks. When conducting the full state space analysis it is recommended to start by generating the *state space report*. The tasks will also require using some of the more advanced query functions available in CPN Tools. These query functions are documented in the <a href="http://wiki.daimi.au.dk/cpntools-help/use_state_space_tool.wiki?cmd=get&anchor=Use+State+Space+Tool">State Space Tool Manual.

### Task 1: Simple Protocol with Bounded Retransmission

Integrate your solution to exercise 3 from project 0 into the <a href="../models/chapter7/7-2LimitProtocol.cpn">CPN model</a> of the simple protocol from Chap 7 (or the other way around).

Investigate the correctness of this variant of the simple protocol in a similar way as explained for the basic simple protocol in Chap 7. You should start by considering a small number of packets (2-3) to be transmitted and a small value of the retransmission limit (e.g., 2). The query functions `ListDeadMarkings` and `HomeSpace` might be useful. Investigate the protocol for different values of the protocol parameters.</p>

### Task 2: Sliding Window Protocol

In <a href="./project1.html">project 1</a> on CPN modelling you developed a CPN model in task 2 (or 3) specifying a sliding window protocol.

Integrate your solution to task 2 (or 3) from project 1 into the <a href="../models/chapter7/7-2LimitProtocol.cpn">CPN model</a> of the simple protocol from Chap 7 of [1] (or the other way around).

Use state space analysis to verify your sliding window protocol model. If you discover errors in your protocol, try to find a counter example and try also to fix any identified errors.
