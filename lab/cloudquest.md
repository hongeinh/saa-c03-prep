## VPC Peering
Service A and Service B are in different VPCs. A depends on B to get report (A wants to connect to B).

1. VPC -> Peering Connection -> Add VPC Peering connection
- Requester: A's CIDR block
- Accepter: B's CIDR block

2. A's subnet -> Route tables -> Route -> Add rule -> Add IPv4 to the peering connection

3. B's subnet -> Route tables -> Route -> Add rule -> Add IPv4 to the peering connection

4. B's security group -> add inbound rule -> IPv4 from custom A's CIDR block