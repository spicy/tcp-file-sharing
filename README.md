# TCP File Sharing

A simple Python-based TCP client-server file sharing application that allows users to upload, download, and list files between a client and server over a TCP connection.

## Features

- **File Transfer**: Upload (`put`) and download (`get`) files between the client and server.
- **File Listing**: List available files on the server.
- **Multi-client Support**: Supports multiple clients connected to the server.
- **TCP Connection**: Communication is handled via TCP sockets.

## Programming Language Used:

Python

## How To Execute Program:

Note: The `server.py` file needs to be ran in the same directory where the `files` folder is located. The uploads will be placed in the `files` directory. Also, the `client.py` file can take either a domain name or an IP address.

1. Start the server

```
python3 server.py <port number>
ex: python3 server.py 21
```

2. Start the client(s)

```
python3 client.py <server machine> <port number>
ex: python3 client.py localhost 21
```

3. Input commands into the client terminal(s):

- ls command

```
ftp> ls
```

Lists out the files currently in the `files` directory on the server.

- put command

```
ftp> put <filename>
```

Client uploads a file to the server. The server will download the file and put it in the `files` directory.

- get command

```
ftp> get <filename>
```

Client downloads a file from the server's `files` directory.

- quit command

```
ftp> quit
```

Client quits the server by closing the control connection between the client and server.

## Misc

- Has unit tests using .txt files in order to reinforce data partitioning, three for client unit test, five for server unit test
- Running the `client.py` and `server.py` files will require being in the same directory where the `files` folder is located in order to properly download and upload files
- Requires Python 3.9.6 or greater


## Team Members: 

- Daniel Currey - dcurrey@csu.fullerton.edu
- Kyle Lee - ipark604@csu.fullerton.edu
- Brett Chiu - brettc@csu.fullerton.edu
- Luke Pina - lukepina@csu.fullerton.edu
- Jonathan Gaytan - jagaytan@csu.fullerton.edu
