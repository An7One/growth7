# Chapter 01 Tour of Systems

## 1.1 Information is Bits + Context

## 1.2 Programs are Translated by other Programs into Different Forms

compilation system

<ul>
    <li>preprocessor</li>
    <li>compiler</li>
    <li>assembler</li>
    <li>linker</li>
</ul>

## 1.3 It Pays to Understand How Compilation Systems Work

<ul>
    <li>Optimizing program performance</li>
    <li>Understanding link-time errors</li>
    <li>Avoiding security holes</li>
</ul>

## 1.4 Processors Read and Interpret Instructions Stored in Memory

### 1.4.1 Hardware Organization of a System

#### Buses

#### I/O Devices

Each I/O device is connected to the I/O bus by either a <i>controller</i> or an <i>adapter</i>.

#### Main Memory

The <i>main memory</i> is a temporary storage device that holds both a program and the data it manipulates while the processor is executing the program.

#### Processor

CPU

Program Counter (PC)

ALU

<ul>
    <li>Load</li>
    <li>Store</li>
    <li>Operate</li>
    <li>Jump</li>
</ul>

microarchitecture

### 1.4.2 Running the <code>Hello</code> Program

<i>direct memory access</i> (DMA)


## 1.5 Caches Matter

<i>processor-memory gap</i>

<i>cache memories</i>

<i>L1 cache</i>

<i>static random access memory</i> (SRAM)

<i>locality</i>

## 1.6 Storage Devices Form a Hierarchy

<i>memory hierarchy</i>

## 1.7 The Operating System Manages the Hardware

### 1.7.1 Processes

A <i>process</i> is the operating system's abstraction for a running program.

<i>context switching</i>

### 1.7.2 Threads

### 1.7.3 Virtual Memory

<i>Virtual memory</i> is an abstraction that provides each process with the illusion that it has exclusive use of the main memory.

<i>virtual address space</i>

figure 1.13

### 1.7.4 Files

A <i>file</i> is a sequence of bytes.

## 1.8 Systems Communicate with Other Systems Using Networks

## 1.9 Important Themes

### 1.9.1 Amdahl's Law

### 1.9.2 Concurrency and Parallelism

#### Thread-Level Concurrency

#### Instruction-Level Parallelism

#### Single-Instruction, Multiple-Data (SIMD) Parallelism

### 1.9.3 The Importance of Abstractions in Computer Systems

## 1.10 Summary

