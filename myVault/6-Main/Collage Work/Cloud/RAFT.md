tag : [[Cloud Computing]] 


### 1. Roles in RAFT

In a RAFT cluster, there are three types of roles for servers:

- **Leader**: The main server that handles all requests and coordinates the updates.
- **Follower**: A passive server that just receives updates from the Leader.
- **Candidate**: A server that tries to become the Leader when there’s no current Leader.

Only one Leader exists at a time, and all other servers are Followers (unless they’re temporarily Candidates).

### 2. How RAFT Elects a Leader

- All servers start as Followers. If a Follower doesn’t hear from a Leader for a while, it becomes a Candidate and starts an election.
- The Candidate asks other servers (Followers) for their votes.
- If the Candidate gets a majority of votes, it becomes the Leader. If no one wins, the process restarts until a Leader is chosen.

This Leader election happens quickly to minimize downtime.

### 3. How the Leader Manages Updates

- When a client sends a request (like adding data), it goes to the Leader.
- The Leader creates a log entry with this data and sends it to all Followers.
- Followers copy the log entry and respond to the Leader, confirming they got it.
- Once the Leader gets confirmations from a majority, it finalizes (commits) the entry and tells all Followers to do the same.

### 4. Handling Failures

If the Leader fails, the Followers notice it isn’t sending updates. They start an election to pick a new Leader. The new Leader then synchronizes logs with other Followers, ensuring consistency is maintained.