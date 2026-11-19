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
2. Do the two threads execute independently?
3. Why might the output order change when the program is executed again?
4. What is the difference between sequential and concurrent execution?

### Thread Synchronization
1. Why does the main program wait when join() is used?
2. What happens when join() is removed?
3. In what situations is thread synchronization necessary?

### Thread Lock
1. What is a shared resource?
2. What is a race condition?
3. What is the purpose of threading.Lock()?
4. What is a critical section?
5. Why is synchronization important when multiple threads access shared data?

### General Questions
1. What is the difference between a process and a thread?
2. What are the advantages of using multithreading?
3. How does multithreading improve application responsiveness?
4. What is the difference between concurrency and parallelism?
5. Why is a lock necessary when multiple threads access shared data?
6. What might happen if a thread is not properly synchronized?
7. Can multiple threads execute simultaneously on a single-core processor? Explain.
8. How does the operating system manage kernel-level threads?