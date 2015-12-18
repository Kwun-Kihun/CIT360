Threads, Executors, Runnables, Handlers

1. Threads

Multithreading refers to two or more tasks executing concurrently within a single program. A thread is an independent path of 
execution within a program. Many threads can run concurrently within a program. Every thread in Java is created and controlled by the java.lang.Thread class. A Java program can have many threads, and these threads can run concurrently, either asynchronously or synchronously.

There are two ways to create thread in java, Implement the Runnable interface (java.lang.Runnable) and By Extending the Thread class (java.lang.Thread)

2. Executors

Factory and utility methods for Executor, ExecutorService, ScheduledExecutorService, ThreadFactory, and Callable classes defined in this package. This class supports the following kinds of methods:

Methods that create and return an ExecutorService set up with commonly useful configuration settings.
Methods that create and return a ScheduledExecutorService set up with commonly useful configuration settings.
Methods that create and return a "wrapped" ExecutorService, that disables reconfiguration by making implementation-specific methods inaccessible.

Executors are capable of running asynchronous tasks and typically manage a pool of threads, so we don't have to create new threads manually.

3. Runnables

The Runnable interface should be implemented by any class whose instances are intended to be executed by a thread. The class must define a method of no arguments called run. This interface is designed to provide a common protocol for objects that wish to execute code while they are active. For example, Runnable is implemented by class Thread. Being active simply means that a thread has been started and has not yet been stopped.

The Runnable interface is used to define a certain task that we want to execute, and the whole implementation of this task is inside its only method, run() (which accepts no arguments). The Runnable class by itself does not create a separate thread, because this is what Thread actually does.

In addition, Runnable provides the means for a class to be active while not subclassing Thread. A class that implements Runnable can run without subclassing Thread by instantiating a Thread instance and passing itself in as the target. In most cases, the Runnable interface should be used if you are only planning to override the run() method and no other Thread methods. This is important because classes should not be subclassed unless the programmer intends on modifying or enhancing the fundamental behavior of the class.

4. Handlers

A Handler allows to send and process Message and Runnable objects associated with a thread's MessageQueue. Each Handler instance is associated with a single thread and that thread's message queue. When it create a new Handler, it is bound to the thread / message queue of the thread that is creating it from that point on, it will deliver messages and runnables to that message queue and execute them as they come out of the message queue.

There are two main uses for a Handler: (1) to schedule messages and runnables to be executed as some point in the future; and (2) to enqueue an action to be performed on a different thread than its own.

When posting or sending to a Handler, you can either allow the item to be processed as soon as the message queue is ready to do so, or specify a delay before it gets processed or absolute time for it to be processed. The latter two allow you to implement timeouts, ticks, and other timing-based behavior.

This is shaing video about the topic. http://youtu.be/zDN1NDOrScc
