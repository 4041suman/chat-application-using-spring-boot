# chat-application-using-spring-boot

Introduction
This project is a realtime chat application developed using Spring Boot and WebSocket. The application allows users to join, chat, and leave chat rooms in real-time. Spring Boot provides a robust and scalable architecture for the application, while WebSocket enables real-time communication between the server and clients. The application has features such as joining chat rooms, sending messages, and leaving chat rooms, providing a seamless and interactive chatting experience for its users.

Websocket
WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. WebSocket is distinct from HTTP.

The protocol enables interaction between a web browser (or other client application) and a web server with lower overhead than half-duplex alternatives such as HTTP polling, facilitating real-time data transfer from and to the server.

Once a websocket connection is established between a client and a server, both can exchange information until the connection is closed by any of the parties.

This is the main reason why WebSocket is preferred over the HTTP protocol when building a chat-like communication service that operates at high frequencies with low latency.

Stomp JS
Simple (or Streaming) Text Oriented Message Protocol (STOMP), formerly known as TTMP, is a simple text-based protocol, designed for working with message-oriented middleware (MOM). It provides an interoperable wire format that allows STOMP clients to talk with any message broker supporting the protocol.

Since websocket is just a communication protocol, it doesn't know how to send a message to a particular user. STOMP is basically a messaging protocol which is useful for these functionalities.

Sock JS
SockJS is used to enable fallback options for browsers that don't support WebSocket. The goal of SockJS is to let applications use a WebSocket API but fall back to non-WebSocket alternatives when necessary at runtime, i.e. without the need to change application code.

Under the hood, SockJS tries to use native WebSockets first. If that fails, it can use a variety of browser-specific transport protocols and presents them through WebSocket-like abstractions.



Dependencies
This code relies on the following imports:

import lombok.*: Lombok library annotations for generating boilerplate code.
Class Declaration
@Getter: Annotation indicating that Lombok should generate getter methods for all fields.
@Setter: Annotation indicating that Lombok should generate setter methods for all fields.
@AllArgsConstructor: Annotation indicating that Lombok should generate a constructor with all fields as arguments.
@NoArgsConstructor: Annotation indicating that Lombok should generate a default constructor with no arguments.
@Builder: Annotation indicating that Lombok should generate a builder method for the class.
Fields
content: Represents the content of the chat message.
sender: Represents the sender of the chat message.
type: Represents the type of the chat message, which is defined as an enum called MessageType.
Enum: MessageType
This enum defines the possible types of chat messages: CHAT, LEAVE, and JOIN.

Methods
The class also includes getter and setter methods for each field to access and modify their values.

getContent(): Returns the content of the chat message.
setContent(String content): Sets the content of the chat message.
getSender(): Returns the sender of the chat message.
setSender(String sender): Sets the sender of the chat message.
getType(): Returns the type of the chat message.
setType(MessageType type): Sets the type of the chat message.
This class serves as a model for chat messages in the application. It encapsulates the content, sender, and type of a chat message. The Lombok annotations eliminate the need to write repetitive boilerplate code for getters, setters, constructors, and builders, making the class concise and easier to work with.
