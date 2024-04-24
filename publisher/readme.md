## How many data your publisher program will send to the message broker in one run? 
The publisher program will transmit five sets of data to the message broker with each execution. This occurs because within the main function, there are five occurrences of publish_event, and each one dispatches a single UserCreatedEventMessage to the message broker.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
The URL "amqp://guest:guest@localhost:5672" in both the publisher and subscriber programs means that they communicate with the same message broker. The messages sent by the publisher will be received by the subscriber.