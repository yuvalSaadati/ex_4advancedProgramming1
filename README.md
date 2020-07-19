# ex_4advancedProgramming1
Advanced Programming 1
# Searching Algorithms Server

### Link to [Github](https://github.com/yuvalSaadati/ex4)

## Description

A programming solving searching problems using Algorithms. 

 ## Compile & Run

* first, you need to pass your listening port by argument to main.
* then, you just run the program and you'll get a message: "Server in now listening..."
* now you can try to connect with clients - send some problems and get solution. 
* the solution will be represented in txt files by the solution number.

## Contributing

### Parallel and Serial

You can see two different files for connecting clients:

* 'MySerialServer' - getting clients one by one.

* 'MyParallelServer' - getting up to 10 clients at the same time. 

  Notice: in our program we use the parallel Server and you can change it to the Serial in the *main.h* class.

### Algorithms

We provided 4 searching algorithms:

* Best First Search

* Breadth First Search

* Depth First Search

* A*

  Notice: in our program we're using the A* Algorithm, although as you can see in the PDF the Best First Search Algorithm is sometimes better than A*. You can change to a different algorithm in *ObjectAdapter.h* class.

### About the program

The main is getting the listening port, creating type of client handler and call the parallel server with both port and clientHandler. The parallel server opens the port for listening and getting clients. While a client send a problem, the *parallelServer* send it to the *clientHandler*. Then, the client handler check if there already has a solution in the *FileCacheManager*. If it doesn't, the *ObjectAdapter* will get the problem, send it to A* Algorithm and return the Solution. 

Notice that the problem is a *SearchableMatrix* object  and the Solution is a string that contains the trace.

We also have a *Point* class for the matrix cells.
