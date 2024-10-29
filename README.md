## Overview
This project is a multi-threaded client-server chat application developed in C++. It enables real-time communication between multiple clients and a server, allowing users to send and receive messages in a chat room environment.

## Features
- **Real-Time Messaging**: Users can send and receive messages instantly.
- **Multi-User Support**: The server can handle multiple clients simultaneously using threads.
- **Dynamic User Naming**: Clients can enter their names, which are displayed with their messages.
- **Color-Coded Output**: Messages are color-coded for better visibility and user experience.

## Technologies Used
- **C++**: The primary programming language used for developing the application.
- **Socket Programming**: For establishing communication between the client and server.
- **Multi-threading**: To handle multiple clients concurrently.

## C++ Features Used
### 1. **Socket Programming**
- Utilized C++ sockets for creating a communication channel between the server and clients. This allows for reliable message transmission over TCP/IP.
- The server listens for incoming connections, while clients initiate a connection to the server.

### 2. **Multithreading**
- Implemented the `<thread>` library to create a new thread for each client connection. This enables concurrent handling of multiple clients, ensuring that messages can be sent and received without delays.
- Each client operates in its own thread, allowing for independent message processing.

### 3. **Mutexes for Thread Safety**
- Employed the `<mutex>` library to prevent data races when multiple threads attempt to modify shared resources, such as the list of connected clients.
- This ensures that the application remains stable and consistent, preventing crashes or corrupted data.

### 4. **String Manipulation and Input Handling**
- Utilized the `std::string` class for handling user names and messages, providing easy manipulation and dynamic sizing.
- The application uses `cin.getline()` for input handling, allowing for names and messages to be captured safely without buffer overflows.

### 5. **Error Handling**
- Comprehensive error handling is integrated throughout the application, particularly for socket operations. This ensures that the application can gracefully handle unexpected issues, such as connection failures.


