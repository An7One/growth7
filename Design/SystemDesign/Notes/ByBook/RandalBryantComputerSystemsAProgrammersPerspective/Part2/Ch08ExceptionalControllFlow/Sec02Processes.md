# Chapter 08 Exceptional Control Flow
## 8.2 Processes

A process is <i>an instance of a program in execution</i>. Each program in the system runs in the <i>context</i> of some process.

### 8.2.1 Logical Control Flow


### 8.2.2 Concurrent Flows

A logical flow whose execution overlaps in time with another flow is called a <i>concurrent flow</i>, and the two flows are said to <i>run concurrently</i>.

The general phenomenon of multiple flows executing concurrently is known as <i>concurrency</i>. The notion of a process taking turns with other processes is also known as <i>multitasking</i>. Each time period that a process executes a portion of its flow is called a <i>time slice</i>. Thus, multitasking is also referred to as <i>time slicing</i>.

If two flows are running concurrently on different processor cores or computers, then they are <i>parallel flows</i>, that they are <i>running in parallel</i>, and have <i>parallel execution</i>.


### 8.2.3 Private Address Space

A process provides each program with its own <i>private address space</i>. This space is private in the sense that a byte of memory associated with a particular address in the space cannot in general be read or written by any other process.


### 8.2.4 User and Kernel Modes

<i>kernel mode</i>


<i>priviledged instructions</i>


### 8.2.5 Context Switches

<i>context switch</i>


<i>page table</i>


<i>process table</i>


<i>file table</i>


<ul>
    <li>to save the context of the current process</li>
    <li>to restore the saved context of some previously preempted process</li>
    <li>to pass control to this newly restored process</li>
</ul>