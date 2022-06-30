### **Messaging Queues**

## **What are Messaging Queues?**
Message queuing makes it possible for applications to communicate asynchronously, by sending messages to each other via a queue. A message queue provides temporary storage between the sender and the receiver so that the sender can keep operating without interruption when the destination program is busy or not connected. Asynchronous processing allows a task to call a service, and move on to the next task while the service processes the request at its own pace.

![alt text](https://www.cloudamqp.com/img/blog/thumb-mq.jpg)

A queue is a line of things waiting to be handled — in sequential order starting at the beginning of the line. A message queue is a queue of messages sent between applications. It includes a sequence of work objects that are waiting to be processed.

A message is the data transported between the sender and the receiver application; it’s essentially a byte array with some headers on top. An example of a message could be an event. One application tells another application to start processing a specific task via the queue.

The basic architecture of a message queue is simple, there are client applications called producers that create messages and deliver them to the message queue. Another application, called a consumer, connects to the queue and gets the messages to be processed. Messages placed onto the queue are stored until the consumer retrieves them.

![alt text](https://miro.medium.com/max/1230/0*kworctnDN9P4jzZf.png)

## **Why they are used?**

Let's suppose there are two processes and they want to communicate, where the first process is the sender and the other is the receiver. Now when the sender sends the data to the receiver and the receiver tries to receive that data here we need message queues. 

A message queue provides an asynchronous communications protocol, which is a system that puts a message onto a message queue and does not require an immediate response to continue processing. Email is probably the best example of asynchronous communication. When an email is sent, the sender continues to process other things without needing an immediate response from the receiver. But it does not strictly follow FIFO order. For every message, two things are always present the first is the data bytes and its type fields.

## **Major System Calls-**

*msget()- 
We used this call to create a new queue or to open an existing queue.

*msgsnd()-
It helps to write a message queue.

*msgrcv()-
It helps to read a message queue.

*msgctl()-
It helps to perform the control operation on a message queue.

## **Popular Software for Messaging Queues-**

1.MuleSoft Anypoint Platform 
2.IBM MQ 
3.Apache Kafka
4.Apache Qpid 
5.Azure Scheduler
6.RabbitMQ
7.Azure Queue Storage
8.TIBCO Rendezvous
9.IBM Cloud Pak for Integration
10.Google Cloud Pub/Sub

## **References**

*https://www.cloudamqp.com/blog/what-is-message-queuing.html

*https://www.g2.com/categories/message-queue-mq

*https://www.youtube.com/watch?v=T__LsWRgNmY

*https://medium.com/must-know-computer-science/system-design-message-queues-245612428a22


