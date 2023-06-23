![Logo](https://upload.wikimedia.org/wikipedia/commons/7/71/RabbitMQ_logo.svg)

## How it works?

![Scheme](https://raw.githubusercontent.com/jellyBott/RabbitMQ/master/Images/rabbitMQ_scheme.jpg)

## Publisher 📨

In RabbitMQ, a publisher is responsible for sending messages to the message broker. The publisher creates messages and publishes them to specific message queues or exchanges within RabbitMQ, allowing other components, known as consumers, to receive and process those messages.

## Exchange ⚙️

An exchange is a message routing agent that receives messages from publishers and routes them to the appropriate message queues based on certain rules. It acts as a mediator between publishers and consumers within the messaging system.

**Types of exchanges:**

 - **Direct** ⚖️
	 - A direct exchange routes messages based on a matching routing key. When a message is published to a 		direct exchange, it is delivered to the queue(s) whose binding key exactly matches the routing key of the message. In other words, the routing key serves as a filter for message routing.
 - **Fanout** 🔗
	 - A fanout exchange broadcasts messages to all queues that are bound to it. It ignores the routing key and simply copies the message to all the queues it knows. This exchange type is useful when you want to deliver the same message to multiple consumers or distribute messages for parallel processing.
- **Topic** 🛃
	 - A topic exchange routes messages based on wildcard patterns defined in the routing keys. The routing key is a string containing multiple words separated by dots. Queues are bound to the exchange using routing patterns that use "*" (wildcard for one word) or "#" (wildcard for zero or more words) to match specific routing keys.

## Queue 🟥 🟧 🟨 🟩 🟦

In RabbitMQ, a queue is a buffer that holds messages until they are consumed by a consumer application. It acts as a temporary storage location for messages within the messaging system. The messages in a queue can be consumed in a [first-in, first-out (FIFO)](https://en.wikipedia.org/wiki/FIFO_%28computing_and_electronics%29) order.

## Consumer 📮
In RabbitMQ, a consumer is an application or component that receives and processes messages from a message queue. It plays a crucial role in the messaging system by subscribing to specific queues and consuming messages that are published by producers.

## Try RabbitMQ

You can simulate the types of exchanges on the 🔗[Try RabbitMQ](https://tryrabbitmq.com). Examples bellow:

**Direct**
![Direct](https://raw.githubusercontent.com/jellyBott/RabbitMQ/master/gifs/rabbitmq_direct.gif)

**Fanout**
![Fanout](https://raw.githubusercontent.com/jellyBott/RabbitMQ/master/gifs/rabbitmq_fanout.gif)

**Topic**
![Topic](https://raw.githubusercontent.com/jellyBott/RabbitMQ/master/gifs/rabbitmq_topic.gif)
