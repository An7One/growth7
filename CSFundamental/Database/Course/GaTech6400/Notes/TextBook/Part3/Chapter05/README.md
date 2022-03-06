# Chapter 05 The Relational Data Model and Relational Database Constraints

## 5.1 Relational Model Concepts

The relational model represents the database as a collection of <i>relations</i>.

It is called a <b>flat file</b> because each record has a simple linear or <i>flat</i> structure.

When a relation is thought of as a <b>table</b> of values, each row in the table represents a collection of related data values.

### 5.1.1 Domains, Attributes, Tuples, and Relations

A <b>domain</b> D is a set of atomic values. By <b>atomic</b> we mean that each value in the domain is indivisible as far as the formal relational model is concerned.

A <b>data type</b> or <b>format</b> is also specified for each domain.

A <b>relation schema</b> R, denoted by <i>R(A1, A2, ..., An)</i>, is made up of a relation name <i>R</i> and a list of attributes, <i>A1, A2, ..., An</i>. Each <b>attribute</b> <i>Ai</i> is the name of a role played by some domain <i>D</i> in the relation schema <i>R</i>. <i>D</i> is called the <b>domain</b> of <i>Ai</i> and is denoted by <b>dom(Ai)</b>. A relation schema is used to describe a relation; <i>R</i> is called the <b>name</b> of this relation. The <b>degree</b> (or <b>arity</b>) of a relation is the number of attributes n of its relation schema.

### 5.1.2 Characteristics of Relations

#### Ordering of Tuples in a Relation

A relation is defined as a <i>set</i> of tuples. Mathmatically, elements of a set have no order among them; hence, tuples in a relation do not have any particular order.

#### Ordering of Values within a Tuple and an Alternative Definition of a Relation

An <b>alternative definition</b> of a relation can be given, making the ordering of values in a tuple <i>unnecessary</i>. In this definition, a relation schema R = {A1, A2, A3, ..., An} is a set of attributes (instead of an ordered list of attributes), and a relation state r(R) is a finite set of mappings r = {t1, t2, ..., t,}, where each tuple <i>ti</i> is a <b>mapping</b> from <i>R</i> to <i>D</i>, and <i>D</i> is the <b>union</b> (denoted by ) of the attribute domains.

According to this definition of tuple as a mpping, a <b>tuple</b> can be considered as a <b>set</b> of (<attribute>, <value>) pairs, where each pair gives the value of the mapping from an attribute <i>Ai</i> to a value <i>vi</i> from <i>dom(Ai)</i>.

When the attribute name and value are included together in a tuple, it is known as <b>self-describing data</b>, because the description of each value (attribute name) is included in the tuple.

We will mostly use the <b>first definition</b> of relation, where the attributes are <i>ordered</i> in the relation schema and the values within tuples are <i>similarly ordered</i>, because it simplifies much of the notation.

#### Values and NULLs in the Tuples

#### Interpretation (Meaning) of a Relation

### 5.1.3 Relational Model Notation

## 5.2 Relational Model Constraints and Relational Database Schemas

### 5.2.1 Domain Constraints

### 5.2.2 Key Constraints and Constraints on NULL Values

### 5.2.3 Reltional Databases and Relational Database Schemas

A <b>relational database schema</b> <i>S</i> is a set of relation schemas S = {R1, R2, ..., Rm} and a set of <b>integrity constraints</b> IC. A <b>relational database state</b> DB of S is a set of relation states DB = {r1, r2, ..., rm} such that each <i>ri</i> is a state of Ri and such that the ri relation states satisfy the integrity constraints specified in IC.

A database state that does not obey all the integrity constraints is called <b>not valid</b>, and a state that satisfies all the constraints in the defined set of integrity constraints IC is called a <b>valid state</b>.

### 5.2.4 Entity Integrity, Referential Integrity, and Foreign Keys

The <b>entity integrity cosntraint</b> states that no primary key value can be NULL.

Key constraints and entity integrity constraints are specified on individual relations. The <b>referential integrity constraint</b> is specified between two relations and is used to maintain the consistency among tuples int he two relations.

### 5.2.5 Other Types of Constraints
<b>constraint specification langauge</b>

<b>triggers</b> and <b>assertions</b>

<b>state constraints</b>

<b>transition constraints</b>

## 5.3 Update Operations, Transactions, and Dealing with Constraints

The operations of the relational model can be categorized into <i>retrievals</i> and <i>updates</i>.

The <b>result relation</b> becomes the answer to (or result of) the user's query.

<b>insert</b>

<b>delete</b>

<b>update</b> (or <b>modify</b>)

### 5.3.1 The Insert Operation

The <b>Insert</b> operation provides a list of attribute values for a new tuple <i>t</i> that is to be inserted into a relation <i>R</i>.

### 5.3.2 The Delete Operation

The <b>Delete</b> operation can violate only referential integrity.

<b>restrict</b>

<b>cascade</b>

<b>set null</b> or <b>set default</b>

### 5.3.3 The Update Operation

The <b>Update</b> (or <b>Modify</b>) operation is used to change the values of one or more attributes in a tuple (or tuples) of some relation <i>R</i>.

### 5.3.4 The Transaction Concept

A <b>transaction</b> is an executing program that includes some database operations. At the end of the transaction, it must leave the database in a valid or consistent state that satisfies all the constraints specified ont he database schema.

A large number of commercial applications running against relational databases in <b>online transaction processing (OLTP)</b> systems are executing transactions at rates taht reach several hundred per second.

## 5.4 Summary