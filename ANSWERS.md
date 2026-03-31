# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[A process is an independent program in execution that has its own memory space, resources, and system state, while a thread is a smaller unit of execution that exists within a process and shares the same memory and resources with other threads in that process. One key difference is that processes do not share memory by default, whereas threads share the same address space, making communication between threads much faster and easier. Another difference is creation overhead: creating a new process is more expensive and slower compared to creating a thread, which is lightweight.

In this assignment, threads were used instead of processes because the scheduler simulation requires frequent switching and interaction between tasks. Using threads allows all simulated processes to share data structures such as the processQueue and processMap in SchedulerSimulation.java, which simplifies communication and coordination. For example, each Process is executed using a Thread (new Thread(process)), and the scheduler manages them efficiently using start() and join() without the overhead of inter-process communication.

Therefore, threads are more suitable for this simulation because they provide faster context switching, lower resource usage, and easier data sharing, which are essential for implementing a responsive Round Robin scheduling system.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling, if a process does not finish within its assigned time quantum, it is preempted (stopped temporarily) and moved to the end of the ready queue. This allows other processes to get CPU time before the unfinished process runs again. The process will later be scheduled again when it reaches the front of the queue in the next cycle.

This behavior can be clearly seen in my program output. For example, process P1 does not finish within the time quantum of 4000ms, so it yields the CPU and is added back to the ready queue.]

Example from my output:
```
[▶️ P1 executing quantum [4000ms] 
  ⏸️ P1 completed quantum 4000ms │ Overall progress: 43%
     Remaining time: 5290ms
  ↻ P1 yields CPU for context switch

  ➕ P1 (Priority: 3) added to ready queue │ Burst time: 9290ms

[...]
Ready Queue:
[P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P11 → P12 → P13 → P14 → P15 → P16 → P1]
]
```

**Explanation of example:**
[In this output, P1 executes for one time quantum (4000ms), but it still has 5290ms remaining, so it cannot finish. The scheduler performs a context switch, and P1 is placed at the end of the ready queue. This means other processes (like P3, P4, etc.) get their turn before P1 runs again.

This re-queueing behavior is important for fairness because it ensures that no single process can monopolize the CPU. Every process gets a fair share of CPU time in cycles, which is especially important when there are many processes, as shown in the output with 16 processes.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[In this simulation, each process such as P1 is executed using a thread and goes through the states: New, Runnable, Running, Waiting, and Terminated. These states are connected to specific method calls in the code such as Thread.start(), Thread.join(), and Thread.sleep(). The lifecycle can be observed clearly as the scheduler repeatedly selects P1 and executes it using the Round-Robin algorithm.]

1. **New**: [P1 is in the New state when the thread is first created using new Thread(process) inside the addProcessToQueue() method. At this point, the thread exists in memory but has not started execution yet. It is simply prepared and placed into the ready queue waiting for scheduling.]

2. **Runnable**: [P1 becomes Runnable when the scheduler selects it from the ready queue and calls Thread.start(). This makes the thread ready to run and eligible for CPU scheduling by the JVM. At this stage, it is waiting for the CPU to assign it execution time.]

3. **Running**: [P1 enters the Running state when the JVM starts executing the run() method after Thread.start() is called. During this state, the process actively uses the CPU to execute its time quantum. This is shown in the output when we see messages like “P1 executing quantum [4000ms]”.]

4. **Waiting**: [P1 enters the Waiting state when Thread.sleep() is called inside the run() method to simulate execution time. During this time, the thread is paused and not using the CPU. Also, the main scheduler thread calls currentThread.join(), which causes it to wait until P1 completes its quantum before continuing.]

5. **Terminated**: [P1 reaches the Terminated state when it completes all its execution and its run() method finishes. This happens when the remaining time becomes 0 after several cycles of execution. In the output, this is shown by the message “P1 finished execution!”, indicating that the thread has ended.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
