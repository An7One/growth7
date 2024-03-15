# Chapter 14, Design Youtube

## Step 1, Understand the Problem and Establish Design Scope

### Back of the envolope estimation

TODO

## Step 2, Propose High-Level Design and Get Buy-in

### Video Uploading Flow

### Video Streaming Flow

## Step 3, Design Deep Dive

### Video Transcoding

#### Directed Acyclic Graph (DAG) model

#### Video Transcoding Architecture

##### Preprocessor

4 Responsibilities:

1. Video splitting
2. Split videos by Group of Pictures(GOP) alignment for old clients
3. DAG generation
4. Cache data

##### DAG Scheduler

The DAG scheduler splits a DAG graph into stages of tasks and puts them in the task queue in the resource manager.

##### Resource Manager

It contains 3 queues and 1 task scheduler:

- Task queue
- Worker queue
- Running queue
- Task scheduler

##### Task Worker

##### Temporary Storage

##### Encoded Video

### System Optimization

#### Speed Optimization: Parallelize Video Uploading

#### Speed Optimization: Place Upload Centers Close to Users

#### Speed Optimization: Parallelism Everywhere

#### Safety Optimization: Pre-signed Upload URL

#### Safety Optimization: Protect Your Videos

#### Cost-saving Optimization

### Error Handling

TODO

## Step 4, Wrap Up
