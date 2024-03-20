# Chapter 12: Design a Chat System

## Introduction

TODO

## Step 1 - Understand the Problem and Establish Design Scope

### Functional Requirement

TODO

### Non-Functional Requirement

TODO

### Feature

- 1-1 Chat with Low Delivery Latency
- Small Group Chat (max of 100 people)
- Online Presence
- Multiple Device Support
- Push Notification

### Estimation

TODO

## Step 2 - Propose High-level Design and Get Buy-In

### Technique to simulate server-initiated connections

#### Polling

#### Long Polling

- A client holds the connection open until there are actually new messages available or a timeout threshold has been reached.
- Once the client receives new messages, it immediately sends another request to the server, restarting the process.

Drawback (TODO)

#### WebSocket

TODO

### High-level Design

#### Stateless Service

TODO

#### Stateful Service

TODO

#### Third-party Integration

TODO

#### Scalability

TODO

#### Storage

2 types of data exist in a typical chat system:

1. Generic data, such as user profile, setting, user friends list, etc.
   1. stored in robust and reliable relational database
   2. replication and sharding are common techniques to satisfy availability and scalability requirement
2. Chat history data
   1. TODO

#### Data Model

##### Message Table for 1-1 Chat

TODO: DB Schema

##### Message Table for Group Chat

TODO: DB Schema

## Step 3 - Design Deep Dive

### Service Discovery

### Message Flow

#### 1-1 Chat Flow

#### Message Synchronization across Multiple Devices

#### Small Group Chat Flow

#### Online Presence

##### User Login

##### User Logout

##### User Disconnection

##### Online Status Fanout

## Step 4 - Wrap Up

### Additional talking points

- Support media files
- End-to-end encryption
- Caching messages on the client side
- Improve the load time
- Error handling
  - the chat server error
  - message resent mechanism
