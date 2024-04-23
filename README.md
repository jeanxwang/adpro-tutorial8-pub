# Adpro - Tutorial 8

## Aliyah Faza Qinthara (2206024726)

### How many data your publisher program will send to the message broker in one run?

The publisher program will send **5 messages** to the message broker in one run. Each `publish_event` function call sends one message, and there are 5 such calls in the `main` function.

### The URL of the message broker

The URL for the message broker is `amqp://guest:guest@localhost:5672`. This URL is used in both the publisher and subscriber programs, indicating that they are connecting to the same message broker. In a messaging system, the publisher sends messages and the subscriber receives those messages. The message broker (in this case, running at `localhost:5672`) is the intermediary that routes messages from publishers to subscribers. Therefore, if the publisher and subscriber are using the same URL for the message broker, they are part of the same messaging system, and the subscriber should be able to receive messages published by the publisher.

### RabbitMQ

![Running](https://cdn.discordapp.com/attachments/1030834426126544907/1232334326536998972/image.png?ex=66291447&is=6627c2c7&hm=c79e9360c64bae6822862ca68ec22e99fb615023bbc908ccb80abc6d43615ede&)

When I execute `cargo run` on the publisher (meaning I'm operating the publisher), it dispatches 5 events to the message broker. These events are subsequently received and handled by the subscriber.
![Console](https://cdn.discordapp.com/attachments/1030834426126544907/1232336571466780753/image.png?ex=6629165e&is=6627c4de&hm=7d858958e732a5023ec081a6cf62ae5517918ff5a135e183f052849688101dcd&)
