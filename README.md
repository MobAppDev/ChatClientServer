ChatClientServer
================

Threaded socket-based chat client and server.

Solution:

The threaded socket-based chat application consists the following:

1. Threaded Java Server: The server accepts the connection with the clients on a given
port. The clients post their messages to the server and server pushes back the chat
messages to all clients who are participating in the chat.
2. The Java Client: The client is responsible to connect to the server, send and receive
messages from the server and update the GUI.
3. The Objective-C Client: The client is responsible to connect to the server, send and
receive messages from the server and update the GUI.


Ant build details:

ant –f antBuild.xml <target>

•

Targets print out a message:

targets:
[echo] Targets are targets, clean, prepare, build, executeServer, executeJavaClient and
execduteObjCClient
[echo] The solution is working on: GNUstep

BUILD SUCCESSFUL
Total time: 0 seconds

•

Build target compiles the programs: Java gets compiled into class files in the
project's classes directory, and the Objective-C programs are compiled into an
executable using make file named ‘GNUmakefile’.

•

Clean target removes the executable and class files.

clean:
[delete] Deleting directory d:\asu\Spring2012\Assign2\ShivaniAssign2\classes

[delete] Deleting directory
d:\asu\Spring2012\Assign2\ShivaniAssign2\ChatAppGNUstep.app
[delete] Deleting directory d:\asu\Spring2012\Assign2\ShivaniAssign2\obj

BUILD SUCCESSFUL
Total time: 0 seconds

•

ExecuteServer target initiates Java server program. It takes port number and one
argument.

ant –f antBuild.xml executeServer

•

The executeJavaClient and execduteObjCClient execute the client applications; it
takes three arguments the user name, host and port number. These arguments are
initialized and properties in the antBuild.xml file.

ant –f antBuild.xml executeJavaClient
ant –f antBuild.xml execduteObjCClient
