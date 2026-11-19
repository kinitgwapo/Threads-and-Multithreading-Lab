# Threads and Multithreading Laboratory
## Student Information
- Name: Kenneth O. Restauro
- Section: B186.1
- Date: 11/19/2026
## Laboratory Description
This laboratory demonstrates thread creation,
multithreading, thread coordination, and
shared-resource management using Python.
## Completed Tasks
1. Single Thread
2. Multiple Threads
3. Thread Synchronization using join()

4. Shared Resource Management using Lock()
## Learning Outcomes
- Create and execute threads.
- Demonstrate concurrent execution.
- Explain thread coordination.
- Apply locks to protect shared resources.

## Guide Questions
### Single Thread
1. What is the purpose of threading.Thread()?
    - This is a class constructor, which allows you to configure a thread object.

2. What happens when start() is executed?
    - It starts a thread object's activity.

3. What is the purpose of join()?
    - It is used to block the caller while the thread is executing. When the thread finishes executing, the caller can then resume.

4. What happens if join() is removed?
    - If a thread object is non-daemon, then a finishes main thread simply waits for the other remaining threads to finish before it fully ends, else it stops any running threads abruptly.

### Multiple Threads
1. How many threads are created in the program?
    - 2 threads were created in the program, t1 and t2.

2. Do the two threads execute independently?
    - Yes, both threads are executing independently.

3. Why might the output order change when the program is executed again?
    - The operating system scheduler determines when threads execute, and does not follow the sequence of written code.

4. What is the difference between sequential and concurrent execution?
    - Threads that are run sequentially forces other threads to wait for the currently running thread to finish before they can execute, while a concurrent thread execution means that multiple threads are being run simultaneously through switching them quickly with respect to overhead.

### Thread Synchronization
1. Why does the main program wait when join() is used?
    - join() from threading module blocks the caller or main function until the thread terminates or finishes.

2. What happens when join() is removed?
    - The caller or main function continues while the thread hasn't finished yet.

3. In what situations is thread synchronization necessary?
    - If the main function or another thread requires data from a specific thread before the next logic executes, then thread synchronization is a must.

### Thread Lock
1. What is a shared resource?
    - A global variable that is used by multiple distinct functions is considered as a shared resource.

2. What is a race condition?
    - When multiple tasks updates a shared resource simultaneously without mutex, the data may be malformed.

3. What is the purpose of threading.Lock()?
    - It initializes locking mechanism such as acquire and release lock. When a code acquires a lock, any other code attempting to acquire the same lock will not be permitted and waits until the original task to release its lock.

4. What is a critical section?
    - A specific part of a code where it must not be interrupted by another other logic at all cost.

5. Why is synchronization important when multiple threads access shared data?
    - To prevent any data from updating incorrectly due to race condition where both are supposed to count up, but the other task sees an older data of the shared resource while the other sees a newer version.

### General Questions
1. What is the difference between a process and a thread?
    - A process is a type of task that is executed, which contains multiple logic, typically called a thread that can be run simultaneously with another thread on the same process or waits for a thread to finish. Every threads' heap memory iniside a process is shared globally within the process.

2. What are the advantages of using multithreading?
    - A process where its threads can be run independently would be much faster than a process where its thread are dependent to another thread.

3. How does multithreading improve application responsiveness?
    - For example, a video player that have two threads that are both the video and audio. It would be annoying to watch a video if both threads weren't run concurrently or in parallelism. With multithreading, you would hear the audio and see the video working together simultaneously.

4. What is the difference between concurrency and parallelism?
    - In terms of computer algorithms, concurrency is defined as tasks being executed in an overlapped time from a single core, acting as multiple tasks being run simultaneously by switching quickly. While parallelism is when tasks are truly run simultaneously by assigning tasks to different cores instead of a single core running both tasks.

5. Why is a lock necessary when multiple threads access shared data?
    - Threads share memory. Without a lock, two threads can read and change the same data at the same time, and the result becomes wrong. A lock lets only one thread use the data at a time.

6. What might happen if a thread is not properly synchronized?
    - A race condition can happen. Threads overwrite each other's changes, so data gets corrupted or updates are lost. It can also cause crashes, wrong results, or a deadlock (threads wait for each other forever).

7. Can multiple threads execute simultaneously on a single-core processor? Explain.
    - No, not purely instant. A single core can run only one thread at a time. The operating system switches between threads very fast (time slicing), so they look like the run together. This is concurrency, not true parallelism.

8. How does the operating system manage kernel-level threads?
    - The kernel knows about each thread and schedules it directly. It keeps a record for each thread (registers, stack, state). It decides which thread runs on which core, saves and loads the thread's state during a context switch, and moves threads between states: ready, running, and waiting. If one thread blocks, the kernel can run another thread of the same process.

## Image(s)

<img width="1721" height="268" alt="Four tasks" src="https://github.com/user-attachments/assets/736a992d-a7b4-421f-ab6a-0ecea9a78191" />