# Chapter 08 Exceptional Control Flow
# 8.1 Exceptions

An <i>exception</i> is an abrupt change in the controller flow in the response to some change in the processer's state.

The change in state is known as an <i>event</i>.

### 8.1.1 Exception Handling

<i>exception table base register</i>


<i>kernel mode</i>

### 8.1.2 Classes of Exceptions

Exceptions can be divided into 4 classes:

| Class     | Cause                         | Async or Sync | Return Behavior                         |
| --------- | ----------------------------- | ------------- | --------------------------------------- |
| Interrupt | Signal from I/O device        | Async         | Always returns to the next instruction  |
| Trap      | Intentional exception         | Sync          | Always returns to the next instruction  |
| Fault     | Potentially recoverable error | Sync          | Might return to the current instruction |
| Abort     | Nonrecoverable error          | Sync          | Never returns                           |



#### Interrrupts

<i>Interrupts</i> occur <i>asynchronously</i> as a result of signals from I/O devices that are external to the processor.


#### Traps and System Calls

<i>Traps</i> are <i>intentional</i> exceptions that occur as a result of executing an instruction. Like <i>interrupt</i> handlers, <i>trap</i> handlers return control to the next instruction. The most important use of traps is to provide a procedure-like interface between user program and the kernel, known as a <i>system call</i>.


#### Faults

When a fualt occurs, the procesor transfers control to the fault handler. If the handler is able to correct the error condition, it returns control to the faulting instruction, thereby re-executing it. Otherwise, the handler returns to an <i>abort</i> routine in the kernel that terminates the application program that caused the fault.


#### Aborts

<Aborts> result from unrecoverable fatal errors, typically hardware errors such as parity errors when DRAM or SRAM bits are corrupted.


### 8.1.3 Exceptions in Linux/x86-64 Systems

#### Linux/x86-64 Fualts and Aborts

<ul>
    <li>Divide error</li>
    <li>General protection fault</li>
    <li>Page fault</li>
    <li>Machine check</li>
</ul>

#### System Calls

| Number | Name | Description | Number | Name  | Description                             |
| ------ | ---- | ----------- | ------ | ----- | --------------------------------------- |
| 0      | read | read file   | 33     | pause | to suspend process until signal arrives |