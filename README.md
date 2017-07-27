# traces-jnsm-2017
Traces used in Learning From Network Device Statistics - Journal of Network and Systems Management (JNSM) 2017.

The datasets available in this repository are under the license CC-BY-4.0.
The full terms are describe in the LICENSE.txt file in the root folder and also in the following link:
https://creativecommons.org/licenses/by/4.0/

If you make any use of such datasets, please refer to it as follows:

Rolf Stadler and Rafael Pasquini and Viktoria Fodor. "Learning From Network Device Statistics". 
Submitted to: Journal of Network and Systems Management (Springer JNSM 2017), July 2017.

The authors can be contact through:
rafael.pasquini@ufu.br
stadler@kth.se
vjfodor@kth.se

# Description of traces

Collected statistics for X_cluster, X_port and X_path are stored in csv files. A csv file contains m rows of n features. Each row represents one observation and has a timestamp t indicating when the statistics were measured. Collected service-level metrics for VoD and KV are stored in Y.csv files together with the observation time t. During experiments, X and Y statistics are collected every second on the testbed.

The first row of all csv files brings the labels for the n features in X and the service-level metrics Y.

In X csv files, the label of a given feature x is represented using the strucuture {Index}_FeatureName. The allocated indexes per X csv file are as follows:

X_cluster.csv for VoD service: 
[0,1] - The two network file storage machines; 
[2,3,4] - The three web server and transcoding machines; 
[5] - The HTTP load balancer machine.

X_cluster for KV service:
[0,1,2,3,4,5] - The six KV store nodes.

X_port (VoD and KV services):
[0,1,2,3,4] - The five ports of switch SWC1;
[5,6,7,8,9] - The five ports of switch SWC2;
[10,11,12,13,14] - The five ports of switch SWC3;
[15,16,17,18,19] - The five ports of switch SWC4;
[20,21] - The two ports of switch SWA1;
[22,23] - The two ports of switch SWA2;
[24,25,26] - The three ports of switch SWA3;
[27,28] - The two ports of switch SWA4;
[29,30] - The two ports of switch SWA5;
[31,32,33] - The three ports of switch SWA6;
[34,35,36] - The three ports of switch SWB1;
[37,38] - The two ports of switch SWB2;
[39,40,41] - The three ports of switch SWB3;
[42,43] - The two ports of switch SWB4;

X_path (VoD and KV services):
The labels represent the interfaces along the communication path in between the Client and the Server Cluster.
As mentioned in the paper, this feature set has 48 features since the path has 12 interfaces.
Please check the labels described for X_port in order to check from which switch a given features is observed.

