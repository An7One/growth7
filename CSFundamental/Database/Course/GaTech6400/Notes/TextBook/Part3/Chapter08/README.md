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

<b>asignment operation</b>

<b>RENAME</b>

## 8.2 Relational Algobra Operations from Set Theory

## 8.3 Binary Relational Operations: JOIN and DIVISION

## 8.4 Additional Relational Operations

## 8.5 Examples of Queries in Relational Algebra

## 8.6 The Tuple Relational Calculus

## 8.7 The Domain Relational Calculus

## 8.8 Summary