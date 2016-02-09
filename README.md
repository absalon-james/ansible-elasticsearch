The inventories and groups var presented in this branch describe an elasticsearch cluster with the following.

7 Physical hosts total

- Host 1 - Master node only. Does not do data or querying. Only cluster management.
- Hosts (2 - 3) - Client nodes. Data processing and cluster load balancing happen here. Can also bundle logstash/kibana applications here.
- Hosts (4 - 7) - Data nodes. Each physical host has 2 data nodes. Special care must be given to prevent primary shard and replica pairs from residing on the same host.

Don't allocate more than 30 GB ram to a single node. Doing so prevents java from using pointer compression.

If stacking multiple nodes in a single host, all operating directories must be unique per node. Ideally, even the storage drives would be unique.
