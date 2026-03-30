# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 29, 2026 – 2:00 AM]
**What I did**: Created a GitHub account with my university email, forked the repository, renamed it, and edited the SchedulerSimulation.java file to include my student ID.

**Details**: 
- Signed up for a GitHub account using my university email.
- Forked the assignment repository to my GitHub account.
- Renamed the forked repository to distinguish it from the original.
- Opened the SchedulerSimulation.java file in GitHub’s web editor.
- Added my student ID to the appropriate section of the file.
- Committed the changes directly on GitHub to save my work.

**Challenges**: 
Understanding the correct order of forking, renaming, and editing files directly on GitHub.

**Solution**: 
Re-read the assignment file for guidance, followed the README instructions carefully, and used GitHub’s web interface to edit and commit the file.
**Time spent**: 
40 minutes

---

### Entry 2 - [March 30, 2026 – 12:00 AM]
**What I did**: I worked on implementing Feature (1) Process Priority. I added a priority field to the Process class, updated the constructor to include it, and generated random priority values (1–5) in the main method. I also displayed the priority when each process enters the ready queue.

**Details**: 
- Added a priority field to the Process class.
- Updated the constructor to accept the priority value.
- Generated random priority values (1–5) in the main method when creating processes.
- Attempted to display the priority when processes enter the ready queue.
**Challenges**: 
The priority value was not showing in the output because I forgot to update the print statement after adding the new field.
**Solution**: 
Modified the print statement inside the addProcessToQueue method to include the priority value. After updating it correctly, the priority appeared with each process in the output.
**Time spent**: Approximately two and a half hours

---

### Entry 3 - [March 30, 2026 – 3:30 AM]
**What I did**: I worked on implementing Feature (2) Context Switch Counter, I added a static counter variable that increments every time a new process starts running in the scheduler loop.
**Details**: 
- Added a static counter variable to track context switches.
- Determined the correct place in the scheduler loop to increment the counter.
- Incremented the counter each time a new process is selected from the queue and begins execution.
**Challenges**: 
Initially, I was unsure about the correct position to increment the counter to accurately represent each context switch.
**Solution**: 
Placed the increment statement right after selecting the next process from the queue and before starting its thread. This ensures the counter increases correctly every time a process begins execution.
**Time spent**: 
Approximately an hour and a half
---

### Entry 4 - [March 30, 2026 – 11:15 AM]
**What I did**: 
I worked on displaying the final results and implementing Feature (3) Waiting Time Tracking, I created a table that shows each process’s information, including Process Name, Burst Time, Priority, and Waiting Time, I also tracked and updated each process’s waiting time and calculated the Average Waiting Time for all processes.
**Details**: 
- Added waiting time tracking to each process.
- Updated the waiting time each time a process waited in the queue.
- Created a table to display each process’s information clearly.
- Included Process Name, Burst Time, Priority, and Waiting Time in the table.
- Calculated the Average Waiting Time by summing all waiting times and dividing by the number of processes.
- Ensured the output was formatted neatly and all values were displayed correctly.
**Challenges**: 
Had difficulty organizing the output format and making sure all values, including the updated waiting times, appeared correctly in the table.
**Solution**: 
Adjusted the print statements to include all required values, implemented the waiting time updates for each process, and properly formatted the table. Calculated the average waiting time by summing the waiting times and dividing by the number of processes.
**Time spent**: 
Approximately three and a half hours
---

### Entry 5 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [X hours]

**Most challenging part**: 

**Most interesting learning**: 

**What I would do differently next time**: 
