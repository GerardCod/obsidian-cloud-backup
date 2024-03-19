#Development #SQS 

AWS FIFO queues are designed to enhance messaging between applications when the order of operations and events has to be enforced.

![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt5-q33-i1.jpg)

**MessageGroupId**

The message group ID is the tag that specifies that a message belongs to a specific message group. Messages that belong to the same message group are always processed one by one, in a strict order relative to the message group (however, messages that belong to different message groups might be processed out of order).