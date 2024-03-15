# Chapter 14, Design Youtube

## Step 1, Understand the Problem and Establish Design Scope

### Back of the envolope estimation

TODO

## Step 2, Propose High-Level Design and Get Buy-in

### Video Uploading Flow

#### Flow a: to upload the actual video

TODO - figure

#### Flow b: to update the metadata

TODO - figure

### Video Streaming Flow

## Step 3, Design Deep Dive

### Video Transcoding

TODO

#### Directed Acyclic Graph (DAG) Model

Meta's streaming video engine uses a directed acyclic graph(DAG) programming model, which defines tasks in stages so they can be executed sequentially or parallelly.

TODO: figure - DAG

Tasks that can be applied on a video file:

- Inspection
- Video Encoding
- Thumbnail
- Watermark

#### Video Transcoding Architecture

##### Preprocessor

4 Responsibilities:

1. Video splitting
2. Split videos by Group of Pictures(GOP) alignment for old clients
3. DAG generation
4. Cache data

##### DAG Scheduler

The DAG scheduler splits a DAG graph into stages of tasks and puts them in the task queue in the resource manager.

TODO - figure, DAG scheduler

##### Resource Manager

It contains 3 queues and 1 task scheduler:

- Task queue
  - a priority queue that contains tasks to be executed
- Worker queue
  - a priority queue that contains worker utilization info
- Running queue
  - contains info about the currently running tasks and workers running the tasks
- Task scheduler
  - it picks the optimal task/worker, and instructs the chosen task worker to execute the job

TODO - figure, Resource Manager

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
