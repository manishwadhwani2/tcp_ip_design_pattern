                                         
                                                        TCP_IP_SERVER_DESIGN_PATTERN

Creating connections and sending data across TCP/IP networks requires a sequence of boilerplate calls to multiple operating system level services when using the BSD Sockets API for network programming. This procedure can be laborious and prone to mistakes.

Here In this project the aim is to  create abstractions that wrap socket calls in user-friendly C++ classes to facilitate the creation of connections and data transfers between network peers by applying design pattern thinking.

Understanding that TCP/IP network programs involve three fundamental patterns of usage or behaviors—actively connecting to servers, passively accepting connections from clients, and transferring data between network peers, 
or clients and servers—is essential to designing an object-oriented network programming API. Every behavior points to a different abstraction that can be used in a different class.

Tcp_Connector: Captures the socket methods needed to establish an active connection with a server. This is a factory class that creates TCPStream objects upon server connection establishment from client applications. 
Tcp_Acceptor - Encapsulates the socket mechanisms to passively accept connections from a client. 
Tcp_Stream - This is a factory class that creates TCPStream objects upon server programs connecting to clients. It provides IP address and network I/O techniques.

Build and Run 

Compilation 
make -f makefile.client
make -f makefile.server

Run 
On first terminal Run ./server 9999 localhost

On second terminal Run ./client 9999 localhost


