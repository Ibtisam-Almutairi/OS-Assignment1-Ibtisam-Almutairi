# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

[Before this assignment, I only knew about threads from lectures, but actually working with them made things much clearer. I learned that threads are not separate programs—they share memory and need to be managed carefully. When I added the context switch counter, I had to figure out exactly when one process stops and another starts, which helped me understand why context switching affects performance. I also saw how threads change states using Thread.start() and Thread.join() in my code, watching processes go from waiting to running and back. The waiting time feature taught me that timing is important, and even small mistakes in the calculation gave wrong results. Using Thread.sleep() to simulate execution showed me how we can test scheduling behavior safely. Overall, this assignment made me realize that multithreading is not just about running multiple things at once, but about managing them fairly so that no process is ignored.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[The most challenging part was modifying Features 1 and 2 while rewriting Feature 3 correctly. Since the features interact with each other, a small mistake could affect the output of all processes. Working directly on GitHub added another layer of difficulty because I had to carefully commit changes and make sure I did not lose my work. Tracking waiting time and context switches simultaneously required careful attention to detail. It was also time-consuming to test each feature and ensure the results matched expectations.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[I overcame the challenges by reviewing the code carefully and understanding how each feature interacts with the others. I removed the incorrect implementation of Feature 3 and corrected Features 1 and 2 step by step. I tested each feature individually before combining them to ensure calculations were correct. I also used GitHub’s web interface to carefully edit and commit changes, which helped me keep track of my progress. Following a structured workflow made it easier to identify and fix mistakes. Taking the time to plan and verify each part improved the overall accuracy and output of the program.]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[Multithreading can be used in many real-world applications where several tasks need to run at the same time. For example, web servers use threads to handle many user requests at once, which makes them faster. Video games and graphics programs use threads to handle rendering, physics, and user input at the same time. Even regular programs like text editors or spreadsheets use threads to keep the interface smooth while doing background work. Working on this assignment helped me understand how threads interact and why it’s important to plan and manage them carefully. Multithreading makes programs faster, more efficient, and more responsive to users.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
