tag : [[Cloud Computing]]


Clock synchronization refers to **the process of ensuring that multiple nodes in a distributed system share a common notion of time**. It is essential for tasks like synchronous data acquisition and simultaneous triggering of events in real-time systems.



- Chirtins 
- Npt 
- Berklay



## Cristian's Algorithm

```
T_Client = T_Server + (T2 - T1)/2
```

## NTP

```
Time Offset θ = (T2 - T1) + (T3 - T4)/2
Round-Trip Delay δ = (T4 - T1) - (T3 - T2)
New Time = T4 +θ 
```
