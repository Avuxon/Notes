# Concurrent Programming

Note: Wait() only waits for a direct child, not grandchildren

## Threads
### How not to run threads
Do not create threads and join threads in the same for loops -> will only have 1 thread running at a time, no benefit. 

One loop to create all threads, one loop to join all threads

## Thread Synchronization 
>Forces threads to happen in some relative order.

Prevents two threads from modifying the same variable or structure at the same time - **a critical section**.
(Threads share heap, static local vars and global vars)

**Atomic Operation** - starts to run and finishes without interrupted by other thread.

## Semaphores
>Special global var that contains integer  counter which can only be:
> - initialized to non negative value
> - changed by two operations, P and V

### P(s) or  Wait(s)
- if counter is 0, sleep
- if ccunter > 0, decrement s

### V(s)
- Atomically increments s 
- If s is 0, a random thread (which had P(s)) will be unblocked

### Semaphore function in Pthreads
```c
int sem_init(sem_t *sem, 0, int  value);
int sem_wait(sem_t *sem);
int sem_post(sem_t *sem);
 ```
&mutex 

call wait on &mutex, increment count, and call post in a for loop in  thread function.

## Race Condition
>Occurs when programs results depend on order of execution of threads

**Data race** - when two threads modify same data

**Condition synchronization** - when you control relative order of actions of different threads (only execute if condition is true)

```c
// bank account example: One withdraw thread and one deposit thread 
// one semaphore to make sure two threads can deposit at the same time, one semaphore to makes withdraw is possible (increase semaphore by 1. using withdraw decrements by 1)
```
# Measuring Time

## Types

- *wall time*: total elapsed time taken by the program
- *process time*: amount of time processor executed process
  - *system time*: amount of time program was executed in kernel mode
  - *user time*: amount of time program was executed in user mode
  - system time + user time = process time
- *interval time*: less accurate, measures elapsed time
- *clock cycles*: more accurate, measured in terms of CPU cycles

## Tracking Time

- UNIX keeps all times in UTC so there is no timezones or daylight saving to deal with
- UNIX uses a reference starting point called *epoch* - midnight 1/1/1970

## Functions (time.h)

```C
    clock_t clock(void);                                // returns process time since start of program execution
    time_t time(time_t *val);                           // fills val with current time (implementation-dependent format)
    char *ctime(time_t *val);                           // returns string representation of time in val
    double difftime(time_t time1, time_t time2);        // returns number of seconds between time1 and time2
    struct tm *gmtime(time_t *val);                     // converts time to UTC time
    struct tm *localtime(time_t *val);                  // converts time to local time
    time_t mktime(struct tm *timeptr);                  // converts a struct tm to time_t (as seconds past epoch) 
```