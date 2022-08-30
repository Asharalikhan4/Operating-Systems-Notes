<h1> <span>Lec 01 : </span>Introduction to Operating System </h1>
<p>
An operating system is a software that manages the computer hardware. It acts as an intermediary between the user of a computer and computer hardware. The purpose of an operating system is to provide an environment in which a user can execute programs in a convenient and efficient manner. It records that the hardware must provide appropriate mechanisms to ensure the correct operation of the computer system and to prevent user programs from interfering with the proper operation of the system.
</p>

<h3>Various relevant definitions of Operating System:</h3>

- An operating system is a program that controls the execution of application programs and acts as an interface between the user of a computer and the computer hardware.

- A more common definition is that the operating system is the one program running at all times on the computer (usually called the kernel), with all else being application programs.

- An operating system is concerned with the allocation of resources and services, such as memory, processors, devices, and information. The operating system correspondingly includes programs to manage these resources, such as a traffic controller, a scheduler, memory management module, I/O programs, and a file system.



<h3>Key functions of the Operating System:</h3>

- Convenience: An OS makes a computer more convenient to use.

- Efficiency: An OS allows the computer system resources to be used in an efficient manner.

- Ability to Evolve: An OS should be constructed in such a way as to permit the effective development, testing and introduction of new system functions at the same time without interfering with service


<h1> <span>Lec 02 : </span>Types of Operating System</h1>

<h3>Types of Operating Systems:</h3>


<h6>1. Single Tasking Operating System -</h6>

- This type of Operating System can run only one program at a particular time.
- They allow only one process at a time in the ram. ex - MS-DOS 
- They are very inefficient.

<h6>2. Multiprogramming Operating System -</h6> 

- A computer running more than one program at a time (like running Excel and Firefox simultaneously).

<h6>3. Multitasking Operating System –</h6>

- It is an extension of multiprogramming where we run the process in the time slot mannner.
- Multitasking system are more responsive.
- Tasks sharing a common resource (like 1 CPU).

<h6>4. Multithreading Operating System -</h6>

- This is an extension of multitasking interleaving idea within the process level, at operating system level you have multiple process in an interleaved fashion and in multithreading you have multiple threads running within a process in interleaved fashion.
- More responsive operating system.
- Help us to utilize the CPU in more efficient manner.
- Switching from one thread to another thread is less costly compare to switching between the process.
- it is implemented in almost all operating system. ex -  MacOS, Windows, Linux.

<h6>5. Multiprocessing Operating System -</h6>

- A computer using more than one CPU at a time.
- In this we have multiple processor availble in a computer and our operating system should have the capability to utlise the processors.
- Nowdays all the desktop get the multiprocessing operating system.


<h6>6. Multiuser Operating System -</h6> 

- This refers to the system where multiple users sitting on different computers can access a single OS resource.


# Lec 03 : Multithreading Introduction
- In multitasking we can do the multiple task at the same time. example we can listen the music and browse the web.(Here task is refering to the process).
- In multithreading we can do the multiple things within a process or task. example - downloading something in browser and browsing.

#### Real world examples of multithreading -
1. <b>Word processors</b> - Typing, saving, formatting and spell-checking happen at the same time.
2. <b>Web server</b> - Apache HTTP server uses thread pools.
3. <b>IDEs</b> - Modern IDEs do compiler error checks while you are writing code.
4. <b>Games</b> - In modern games, multiple objects are implemented as different threads.

#### Advantage of multithreading -
- Parallelism and Improved performance.
- Responsiveness.
- Better resource utilization.

#### Disadvantage of multithreading -
- Difficulty in writing, testing and debugging code.
- can lead to deadlock and race condition when you have shared variables.
- Example of race condition -
first it is executed currectly while in the second time second thread croosed the path with the first thread.
![example image](/images/raceCondition.png "Example image")
- Example of deadlock - In multithreading s situation may arise when multiple threads involved in deadlocks and not proceed furthur at all.<br>
![deadlock example](/images/deadlock.png "deadlock example")
<br>
In the upper digram the R1 and R2 is non-shareable resources, only one thread can use one at a time. Here T1 is holding R1 and waiting for the R2 while T2 is waiting for the R1 and holding R2. SO here none of the thread can proceed furthur.



# Lec 04 : Thread vs Process

- When we open application in our computer example word processor, music player they are loaded first from hard disk into RAM and then they become the process, these are typically called process. While these process have multiple thread. Like in the music player one thread is playing the music while the other thread is shuffling the songs. Most of the application is multi-threaded cause multi-threading utilise space better and take advantage of multi-core processor.

#### How process and thread treated by operating system -
Pictorial representation of process with single thread. These are segments of a process.
![deadlock example](/images/singleThread.png "deadlock example")
- If a process is single threaded then it will have only one stack. For multi-threaded processes we have multiple stacks.
![deadlock example](/images/multipleThread.png "deadlock example")
- Multiple threads have multiple stacks but same Heap, data and code.
- Concurrent and parallel have different meanings with reference to process execution.
###### More about threads:
- Faster to create and terminate.
- Share same address space.
- Easier to communicate.
- Context switching is easier.
- Lightweight.