# Chapter 1 Databases and Database Users

## 1.1 Introduction

A <b>database</b> is a collection of related data. By <b>data</b>, we mean known facts that can be recorded and that have implicit meaning. <br/>

A <b>database management system (DBMS)</b> is a computerized system that enables users to the create and maintain a database. The DBMS is a <i>general-purpose software ssytem</i> that facilitates the process of <i>defining, constructing, manipulating,</i> and <i>sharding</i> databases among various user ans applications. <b>Defining</b> a database involves specifying the data types, structures, and constraints of the data to be stored in the database.

<b>meta-data</b>

<b>Constructing</b> the database is the process of storing the data on some storage medium that is controlled by the DBMS. <b>Manipulating</b> a database includes functions such as querying the database to retrieve specific data, updating the database to reflect changes in the miniworld, and generating reports from the data. <b>Sharing</b> a database allows multiple users and programs to access the database simultaneously.

An <b>application program</b> accesses the database by sending queries or requests for data to the DBMS. A <b>query</b> typically cuases some data to be retrieved; a <b>transaction</b> may cause some data to be read and some data to be written into the database.

## 1.2 An Example

## 1.3 Characteristics of the Database Approach

### 1.3.1 Self-Describing Nature of a Database System

### 1.3.2 Insulation between Programs and Data, and Data Abstraction

<b>program-data independence</b>

<b>program-operation independence</b>

The characteristic that allows program-data independence and program-operation independence is called <b>data abstraction</b>. A DBMS provides users with <b>conceptual representation</b> of data that does not include many of the details of how the data is stored or how the operations are implemented. Informally, a <b>data model</b> is a type of data abstraction that is used to provide this conceptual representation.

### 1.3.3 Support of Multiple Views of the Data

### 1.3.4 Sharing of Data and Multiuser Transaction Processing

<b>concurrency control</b>

<b>online trasaction processing (OLTP)</b>

A <b>transaction</b> is an <i>executing program</i> or <i>process</i> that includes one ore more database accesses.

The <b>isolation</b> property ensures taht each transaction appears to execute in isolation from other transactions.

The <b>atomicity</b> property ensures that either all the database operations in a transaction are executed or none are.

## 1.4 Actors on the Scene

### 1.4.1 Database Administratros

### 1.4.2 Database Designers

### 1.4.3 End Users

<b>End users</b> are the people whose jobs require access to the database for querying, updating, and generating reports.

<ul>
    <li>Casual end users</li>
    <li>Native or parametric end users</li>
    <li>Sophisticated end users</li>
    <li>Standalone users</li>
</ul>

### 1.4.4 System Analysts and Application Programmers (Software Engineers)

## 1.5 Workers behind the Scene

<ul>
    <li>DBMS system designers and implementers</li>
    <li>Tool developers</li>
    <li>Operators and maintenance personnel</li>
</ul>

## 1.6 Advantages of Using the DBMS Approach

### 1.6.1 Controlling Redundacy

<b>redundancy</b>

<b>data normalization</b>

<b>controlled redundancy</b>

<b>denormalization</b>

### 1.6.2 Restricting Unauthorized Access

<b>security and authorization subsystem</b>

<b>priviledged software</b>

### 1.6.3 Providing Persistent Storage for Program Objects

<b>persistent storage</b>

<b>object-oriented database system</b>

A complex object in C++ can be stored permanently in an object-oriented DBMS. Such an object is said to be <b>persistent</b>.

<b>impedance mismatch problem</b>

<b>compatibility</b>

### 1.6.4 Providing Storage Structures and Search Techniques for Efficient Query Processing

<indexes>

<b>buffering</b> or <b>caching</b>

The <b>query processing and optimization</b> module of the DBMS is responsible for choosing an efficient query execution plan for each query based on the existing storage structures.

### 1.6.5 Providing Backup and Recovery

The <b>backup and recovery subsystem</b> of DBMS is responsible for recovery.

### 1.6.6 Providing Multiple User Interfaces

<b>graphical user interface (GUIs)</b>

### 1.6.7 Representing Complex Relationships among Data

### 1.6.8 Enforcing Integrity Constants

<b>integrity constraints</b>

<b>referential integrity</b>

<b>key</b> or <b>uniqueness</b>

<b>business rules</b>

<b>inherent rules</b>

### 1.6.9 Permitting Inferencing and Actions Using Rule and Triggers

Some database systems provide capabilities for defining <i>deduction rules for inferencing</i> new information from the stored database facts. Such systems are called <b>deductive database systems</b>.

<b>trigger</b>

<b>stored procedures</b>

<b>active database systems</b>

### 1.6.10 Additional Implictions of Using the Database Approach

## 1.7 A Brief History of Database Applications

### 1.7.1 Early Database Applications Using Hierachical and Network Systems

### 1.7.2 Providing Data Abstraction and Application Flexibility with Relational Databases

### 1.7.3 Object-Oriented Applications and the Need for More Complex Database

### 1.7.4 Interchaging Data on the Web for E-Commerce Using XML

### 1.7.5 Extending Database Capabilites for New Applications

## 1.8 When Not to Use a DBMS

<ul>
    <li>High initial investment in hardware, software, and training</li>
    <li>The generaliity that a DBMS provides for defining and processing data</li>
    <li>Overhead for providing security, concurrency control, recovery, and integrity functions</li>
</ul>

## 1.9 Summary
