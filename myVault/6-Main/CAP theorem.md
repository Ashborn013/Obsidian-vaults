Tag : [[Cloud Computing]]

The **CAP theorem** is a concept in distributed systems that describes a fundamental trade-off between three key properties: **Consistency**, **Availability**, and **Partition Tolerance**. It states that a distributed database can only guarantee two of these three properties at any given time. Let’s break down each part of the theorem in simple terms:

### 1. Consistency (C)

Consistency means that all nodes (servers) in a distributed system see the same data at the same time. For example, if you update a piece of data on one server, that update should immediately appear on all other servers. In other words, each read operation returns the most recent write.

### 2. Availability (A)

Availability means that every request receives a response, either successfully or with an error, and that the system is always operational. In an available system, every node (or at least the system as a whole) is always ready to process requests, even if some nodes are down.

### 3. Partition Tolerance (P)

Partition tolerance means that the system can continue operating even if there are communication breaks (partitions) between nodes. In a partitioned system, some nodes can’t communicate with others due to network issues, but the system can still function despite this temporary split.

### The CAP Trade-Off

According to the CAP theorem, a distributed system can guarantee **only two of the three properties** at once:

- **CP (Consistency and Partition Tolerance)**: The system ensures consistency and can handle network partitions but sacrifices availability. If there’s a network partition, some requests might fail to maintain consistent data.
    
- **AP (Availability and Partition Tolerance)**: The system ensures availability and handles partitions but may have data inconsistencies across nodes. In other words, users may see outdated data temporarily until the system syncs up.
    
- **CA (Consistency and Availability)**: The system is consistent and available but cannot handle network partitions. This combination is typically seen in single-node or tightly coupled systems where partitioning isn’t an issue.
    

### Why CAP Matters

CAP theorem helps architects of distributed systems decide what trade-offs to make depending on the requirements of the system. For example:

- In banking (where consistency is critical), CP systems are often preferred to ensure accurate data.
- In social media (where availability is prioritized), AP systems might be used, allowing for some temporary inconsistency.