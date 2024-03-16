# Chapter 12 - Design a Chat System

## Introduction

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

## Step 2 - Prepare High-Level Design and Get Buy-In

### Polling

### Long Polling

### WebSocket

### High-level Design

#### Stateless Service

#### Stateful Service

#### Third-party Integration

#### Scalability

#### Storage

#### Data Model

##### Message Table for 1-1 Chat

##### Message Table for Group Chat

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
