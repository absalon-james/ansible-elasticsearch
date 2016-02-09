The inventories and groups var presented in this branch describe an elasticsearch cluster with the following.

7 Physical hosts total

Host 1 - Master node only. Does not do data or querying. Only cluster management
Hosts (2 - 3) - Client nodes. Data processing and cluster load balancing happen here. Can also bundle logstash/kibana applications here.
Hosts (4 - 7) - Data nodes. Can stack as many nodes while leaving 50% memory available for os and file system cache. If going multinode, also divide processors.

