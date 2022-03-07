# Chapter 08 The Relational Algebra and Relational Calculus

The basic set of operations for the formal relational model is the <b>relational algebra</b>. These operations enable a user to specify basic retrieval requests as <i>relational algebra expressions</i>.

Whereas the algebra defines a set of operatins for the relational model, the <b>relational calculus</b> provides a higher-level <i>declarative</i> language for specifying relational queries. In a relational calculus expression, there is <i>no order of operations</i> to specify how to retrieve the query result - only what information the result should contain. This is the main distinguishing feature between relational algebra and relational calculus.

<b>unary operation</b>

<b>binary operation</b>

<b>aggregate functions</b>

<b>relational calculus</b>

## 8.1 Unary Relational Operations: SELECT and PROJECT

### 8.1.1 The SELECT Operation

<b>selection condition</b>

<b>clauses</b>

The <b>SELECT</b> operator is <b>unary</b>; that is, it is applied to a single relation. Moreover, the selection operation is applied to <i>each tuple individually</i>; hence, selection conditions cannot involve more than onre tuple. The <b>degree</b> of the relation resulting from a SELECT operation - its number of attributes - is the same as the degree of <i>R</i>.

<b>selectivity</b>

<b>cumulative</b>

<b>cascade</b> (or <b>sequence</b>)

### 8.1.2 The PROJECT Operation

The <b>Project</b> operation selects certain <i>columns</i> from the table and discards the other columns.

<b>degree</b>

<b>duplicate elimination</b>

<b>multiset</b> or <b>bag</b>

<b>DISTINCT</b>

### 8.1.3 Sequences of Operations and the RENAME Operation

<b>relational algebra expression</b>

<b>in-line expression</b>

<b>assignment operation</b>

<b>RENAME</b>

## 8.2 Relational Algobra Operations from Set Theory

### 8.2.1 The UNION, INTERSECTION, and MINUS Operations

<b>UNION</b>

<b>INTERSECTION</b>

<b>SET DIFFERENCE</b> (also called <b>MINUS</b> or <b>EXCEPT</b>)

These are <b>binary</b> operations; that is, each is applied to two sets (of tuples). When these operations are adapted to relational databases, the two relations on which any of these 3 operations are applied must have the same <b>type of tuples</b>; this condition has been called <i>union compatibility</i> or <i>type compatiblity</i>. Two relations R(A1, A2, ..., An) and S(B1, B2, ..., Bn) are said to be <b>union compatible</b> (or <b>type compatible</b>) if they have the same degree n and if <i>dom(Ai) = dom(Bi)</i> for <i>1 <= i <= n</i>. This means that the two relations have the same number of attributes and each corresponding pair of attributes has the same domain.

Both <i>UNION</i> and <i>INTERSECTION</i> are <i>commutative operations</i>.

### 8.2.2 The CARTESIAN PRODUCT (CROSS PRODUCT) Operation

## 8.3 Binary Relational Operations: JOIN and DIVISION

### 8.3.1 The JOIN Operation

### 8.3.2 Variations of JOIN: the EQUIJOIN and NATURAL JOIN

### 8.3.3 A Complete Set of Relational Algebra Operations

### 8.3.4 The DIVISION Operation

### 8.3.5 Notation for Query Trees

## 8.4 Additional Relational Operations

### 8.4.1 Generailized Projection

### 8.4.2 Aggregate Functions and Grouping

### 8.4.3 Recursive Closure Operation

<b>recursive closure</b>

<b>recursive relationship</b>

### 8.4.4 OUTER JOIN Operation

This type of join, where tuples with no match are eliminated, is known as an <b>inner join</b>.

A set of operations, called <b>outer joins</b>, were developed for the case where the user wants to keep all the tuples in <i>R</i>, or all those in <i>S</i>, or all those in both relations in the result of the JOIN, regardless of whether or not they have matching tuples in the other relation.

<b>LEFT OUTER JOIN</b>

<b>RIGHT OUTER JOIN</b>

<b>FULL OUTER JOIN</b>

### 8.4.5 The OUTER UNION Operation

The <b>OUTER UNION</b> operation was developed to take the union of tuples from two relations that have some common attributes, but are <i>not union (type) compatible</i>.

<b>partially compatible</b>

## 8.5 Examples of Queries in Relational Algebra

## 8.6 The Tuple Relational Calculus

<b>relational calculus</b>

<b>tuple relational calculus</b>

<b>domain relational calculus</b>

<b>declarative</b>

<b>nonprocedural</b>

<b>procedural</b>

<b>expressive power</b>

<b>relationally complete</b>


### 8.6.1 Tuple Variables and Range Relations

<b>tuple variables</b>


### 8.6.2 Expressions and Formulas in Tuple Relational Calculus

### 8.6.3 The Existential and Universal Quantifiers

### 8.6.4 Sample Queries in Tuple Relational Calculus

### 8.6.5 Notation for Query Graphs

### 8.6.6 Transforming the Universal and Existential Quantifiers

### 8.6.7 Using the Universal Quantifier in Queries

### 8.6.8 Safe Expressions

## 8.7 The Domain Relational Calculus

<b>domain calculus</b>

<b>domain variables</b>

## 8.8 Summary