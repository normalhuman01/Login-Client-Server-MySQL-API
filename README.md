# Login Client/Server Application with MySQL C API

![Project Logo](.png)

## Overview

This is a client/server application for user login authentication, using Winsock libraries for networking and the MySQL C API for database interactions. Developed by Borys H.N. on 3.13.12 (insert additional project information here).

## Prerequisites

Before getting started, ensure you have the following prerequisites:

1. MySQL Server installed and running:
   - Use the provided SQL script to create the 'Login.users' database and the required table.
   - It is crucial to set up the database and table correctly; otherwise, the program will not function as expected.
   - Ensure MySQL Server is up and running to avoid program termination.

2. Visual C++ or equivalent libraries for handling Winsock operations:
   - The development environment used for this project is Windows Visual Studio C++ Express 2010 on a 64-bit Windows Vista machine.

## Getting Started

Follow these steps to get started with the project:

1. After meeting the prerequisites, create a solution with two projects: 'Client' and 'Server'.

2. Set the 'Client' project's dependency to 'Server', and configure both projects to start simultaneously.

3. Add your code and compile the projects.

   > Note: Be sure to include your MySQL database login information in 'UsersManager.cpp' and edit the server name in 'Server.cpp' if necessary.

4. Run the 'Server' project:
   1. Provide a port number (ensure it matches the one to be used by the 'Client').
   2. Start the server with the 's' option to make it wait for a connection.

5. Run the 'Client' project:
   1. Specify the server's IP address (e.g., 127.0.0.1, localhost, 192.168.0.x).
   2. Enter the port number on which the server is listening.
   3. If everything is set up correctly, press 'c' to establish a connection with the server. The server will assign a unique port number to the connection.
   4. Press 'm' to open the message dialogue and begin communication.

## Future Enhancements

These are some future enhancements planned for the project:

- Resolve server-related AV exceptions.
- Implement encrypted logins for users stored in the database (decryption handled by the server).
- Restrict authentication to root users only for added security.
- Encrypt user names and passwords stored in the MySQL database (currently hard-coded in 'UsersManager.cpp').


