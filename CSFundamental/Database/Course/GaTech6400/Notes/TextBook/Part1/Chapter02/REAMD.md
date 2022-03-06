# Chapter 2 Database System Concepts and Architecture

<b>cloud computing</b>

<b>big data</b>

<b>client module</b>

<b>server module</b>

## 2.1 Data Models, Schemas, and Instances

### 2.1.1 Categories of Data Models

## 2.2 Three-Schema Architecture and Data Independence

### 2.2.1 The Three-Schema Architecture

<ol>
    <li>The <b>internal level</b> has an <b>internal schema</b>, which describes the physical storage structure of the database.</li>
    <li>The <b>conceptual level</b> has a <b>conceptual schema</b>, which describes the structure of the whole database for a community of user</li>
    <li>The <b>external</b> or <b>view level</b> includes a number of <b>external schemas</b> or <b>user views</b>.</li>
</ol>

The process of transforming requests and results between levels are called <b>mappings</b>.

### 2.2.2 Data Independence

<b>Data independence</b> is defined as the capacity to change the schema at one level of a database system without having to change the schema at the nxt higher level.
<oL>
    <li><b>Logical data independence</b> is the capacity to change the conceptual schema without having to change external schema or application programs.</li>
    <li><b>Physical data independece</b>, is the capacity to change the internal schema without having to change the conceptual schema.</li>
</oL>

## 2.3 Database Languages and Interfaces

### 2.3.1 DBMS Languages

### 2.3.2 DBMS Interfaces

## 2.4 The Databse System Environment

### 2.4.1 DBMS Component Modules

### 2.4.2 Databaase System Utilities

<ul>
    <li>Loading</li>
    <li>Backup</li>
    <li>Database storage regonization</li>
    <li>Performance monitoring</li>
</ul>

### 2.4.3 Tools, Application Environments, and Communications Facilities

## 2.5 Centralized and Client/Server Architectures for DBMSs

### 2.5.1 Centralized DMBSs Architecture

### 2.5.2 Basic Client/Server Archiectures

### 2.5.3 Two-Tier Client/Server Architecture for DBMSs

### 2.5.4 Three-Tier and n-Tier Architectures for Web Applications

<b>three-tier architecture</b> includes <i>Client</i>, <i>Application Server</i> or <i>Web Server</i>, and <i>Database Server</i>.

## 2.6 Classification of Database Management Systems

## 2.7 Summary

data model

<ul>
    <li>High-level or conceptual data models (based on entities and relationships)</li>
    <li>Low-level or physical data models</li>
    <li>Representational or implementation data models (record-based, object-oriented)</li>
</ul>

three-schema DBMS architecture

<ul>
    <li>An internal schema describes the physical storage structure of the database</li>
    <li>A conceptual schema is a high-level description of the whole database</li>
    <li>External schemas describe the views of different user groups.</li>
</ul>