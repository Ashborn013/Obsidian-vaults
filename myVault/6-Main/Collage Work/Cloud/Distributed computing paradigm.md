
tag : [[Cloud Computing]]



![[Pasted image 20241110220745.png]]

## Message Passing 

- It is a basic approach for Inter Process Communication
- A process sends a message representing the request
![[Pasted image 20241110220852.png]]


## Client Server Paradigm

- In this approach, the server acts as a service provider, the client issues the request and wait for the response from the serve
![[Pasted image 20241110220943.png]]

## Peer to Peer Paradigm

- anyone can make request to others and get the response.
![[Pasted image 20241110221044.png]]



## Message System Paradigm:
- Message system act as intermediate among independent processes. It is also act as switch through which process exchange messages asynchronously in decoupled manner. sender sends message which drop at first in message system then forward to message queue which is associated with the receiver.
![[Pasted image 20241110221429.png]]


## **Point to Point message model:**

- Unlike the basic message-passing model, it provides asynchronous message passing


## **Public/Subscribe Model:**

- users can subscibe to a topic and litten in the messages in that come into a topic
