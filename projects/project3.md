## Project 3 : CPN Performance Analysis

The project is concerned with performance analysis. The goal is to apply simulation-based performance analysis to investigate the efficiency of a sliding window protocol, and compare it to the performance of the stop-and-wait protocol as presented in Chap. 12.

The project consists of two tasks and relies on the support for performance analysis which is part of CPN Tools. As a preparation for the project, it is recommended that you familiarise yourself with the use of the <a href="http://wiki.daimi.au.dk/cpntools-help/performance_analysis.wiki?cmd=get&anchor=Performance+Analysis">performance analysis</a> and <a href="http://wiki.daimi.au.dk/cpntools-help/monitoring_a_cp-net.wiki?cmd=get&anchor=Monitoring+a+CP-net">monitoring</a> facilities of CPN Tools.

### Task 1: Stop-and-wait protocol performance

Start by considering the <a href="../models/chapter12/12-7PerformanceProtocol.cpn">CPN model</a> of the stop-and-wait protocol from Chap. 12.7. This CPN model includes the data collection monitors required in order to estimate the performance measures defined in Chap. 12 for the stop-and-wait protocol (e.g., queues, packet delay, throughput). </p>

Use simulation replication to investigate the performance of the stop-and-wait protocol in a similar way as described in Chap. 12. Investigate the performance of the protocol for different settings of the protocol parameters.</p>

### Task 2: Sliding window protocol performance</h4>

In <a href="./project1.html">project 1</a> on CPN modelling you developed a CPN model in task 2 (or 3) specifying a sliding window protocol. Integrate your solution to task 2 (or 3) from project 1 into the <a href="../models/chapter12/12-7PerformanceProtocol.cpn">CPN model</a> of the stop-and-wait protocol from Chap 12.7. Investigate the performance of this protocol using simulations in a similar way as was done in task 1 for the stop-and-wait protocol.

Compare the results obtained in this task with the results obtained in task 1. Under what circumstances and in what sense is the sliding-window protocol more efficient that the stop-and-wait protocol? What parameters have the most influence on the performance of two protocols.
