## How many data your publisher program will send to the message broker in one run? 
The publisher program will transmit five sets of data to the message broker with each execution. This occurs because within the main function, there are five occurrences of publish_event, and each one dispatches a single UserCreatedEventMessage to the message broker.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
The URL "amqp://guest:guest@localhost:5672" in both the publisher and subscriber programs means that they communicate with the same message broker. The messages sent by the publisher will be received by the subscriber.

## Running RabbitMQ as message broker
![alt text](image.png)

## Sending and processing event 
![alt text](image-1.png)
As the message broker or RabbitMQ operates, running our Subscriber and Publisher programs (via cargo run) results in the Publisher transmitting data to the message broker, subsequently received by the Subscriber. Illustrated in the provided image, we note that the Publisher sends data once to the message broker, with the Subscriber promptly receiving it.

## Monitoring chart based on publisher
![alt text](image-2.png)

 As depicted in the provided image, I experimented with running the Publisher repeatedly, leading to an escalation in message rates. Subsequently, after a brief pause, I executed it twice more with a slightly extended gap. Through this process, I grasped that message rates surge when the Publisher dispatches data to the message broker. Moreover, a high message rate entails the message broker receiving a substantial volume of data from the Publisher.