# Chapter 3 Data Modeling Using the Entity-Relationship(ER) Model

entity-relationship(ER) model, a high-level conceptual data model.

ER diagram

Unified Modeling Language (UML)

## 3.1 Using High-Level Conceptual Data Models for Database Design

Once the requirements have been collected and analyzed, the next step is to create a <b>conceptual schema</b> for the database, using a high-level conceptual data model. This step is called <b>conceptual design</b>.

The next step in database design is the actual implementation of the database, using a commercial DBMS. Most current commercial DMBSs use an implementation data model - such as the relational (SQL) model - so the conceptual schema is transformed from the high-level data model into the implementation data model. This step is called <b>logical design</b> or <b>data model mapping</b>; its result is a database schema in the implementation data model of the DBMS.

The last step is the <b>physical design</b> phase, during which the internal storage structures, file orgnizations, indexes, access paths, and physical design parameters for the database files are specified.

## 3.2 A Sample Database Application

## 3.3 Entity Types, Entity Sets, Attributes, and Keys

### 3.3.1 Entities and Attributes

#### Entities and their Attributes

The basic concept that the ER model represents is an <b>entity</b>. Each entity has <b>attributes</b>.

#### Composite versus Simple (Atomic) Attributes

<b>Composite attributes</b> can be divided into smaller subparts, which represent more basic attributes within independent meanings.

Attributes that cannot be divided are called <b>simple</b> or <b>atomic attributes</b>.

#### Single-Valued versus Multivalued Attributes

#### Stored versus Derived Attributes

The value of <i>Age</i> can be determined from the current date and value of that person's <i>Birth_date</i>. The <i>Age</i> attribute is hence called a <b>derived attribute</b> and is said to be <b>derived from</b> the <i>Birth_date</i> attribute, which is called a <b>stored attribute</b>.

#### NULL Values

#### Complex Attributes

<b>complex attributes</b>, nested

### 3.3.2 Entity Types, Entity Sets, Keys, and Value Sets

#### Entity Types, Entity Sets, Keys, and Vlaue Sets

An <b>entity type</b> defines a <i>collection</i> (or <i>set</i>) of entities that have the same attributes.

The collection of all entities of a particular entity type in the database at any point in time is called an <b>entity set</b> or <b>entity collection</b>; the entity set is usually referred to using the sanme name as the entity type, even though they are two separate concepts.

An entity type describes the <b>schema</b> or <b>intension</b> for a <i>set of entities</i> that sahre the same structure. The collection of entities of a particular entity type is goruped into an entity set, which is also called the <b>extension</b> of the entity type.

#### Key Attriburtes of an Entity Type

An important constraint on the entities of an entity type is the <b>key</b> or <b>uniqueness constraint</b> on attributes. An entity type usually has one or more attributes whose values are distinct for each individual entity in the entity set. Such as attribute is called a <b>key attribute</b>, and its values van be used to identify each entity uniquely. In ER diagrammatric notation, each key attribute has its name <b>underlined</b> inside the oval.

#### Value Sets (Domains) of Attributes

### 3.3.3 Initial Conceptual Design of the Company Database

## 3.4 Relationship Types, Relationship Sets, Roles, and Structural Constraints

### 3.4.1 Relationship Types, Sets, and Instances

A <b>relationship type</b> R among n entity types E1, E2, ..., En defines a set of associates - or a <b>relationship set</b> - among entities from these entity types.

### 3.4.2 Relationship Degree, Role Names, and Reecursive Relationships

#### Degree of a Relationship Type

A relationship type of degree two is call <b>binary</b>, and one of degree three is called <b>ternary</b>.

#### Relationship as Attributes

#### Role Name and Recursive Relationships

The <b>role name</b> signifies the role that a participating entity from the entity type plays in each relationship instance, and it thelps explain what th relationship means. <br/>

In some cases the same entity type participates more than once in a relationship type in different roles. In such cases, the role name becomes essential for distringuishing the meaning of the role that each participating entity plays. Such relationship types are called <b>recursive relationships</b> or <b>self-referencing relationships</b>.

### 3.4.3 Constraints on Binary Relationship Types

#### Cardinality Ratios for Binary Relationships

The <b>cardinality ratio</b> for a binary relationship specifies the <i>maximum</i> number of relationshp instances that an entity can participate in.

#### Participation Constraints and Existence Dependencies

The <b>participation constraint</b> specifies whether the existence of an entity depends on its being related to another entity via the relationship type. This constraint specifies the <i>minimum</i> number of relationship instances that each entity can participate in and is sometimes called the <b>minimum cardinality constraint</b>.

<b>total participation</b>

<b>existence dependency</b>

<b>partial</b>

<b>structural constaints</b>

### 3.4.4 Attributes of Relationship Types

## 3.5 Weak Entity Types

Entity types that do not have key attributes of their own are called <b>weak entity types</b>. In contrast, <b>regular entity types</b> that do have a key attribute are called <b>strong entity types</b>.

Entities belonging to a weak entity type are identified by being related to specific entities from another entity type in combination with one of their attribute values. We call this other entity type the <b>identifying</b> or <b>owner entity type</b>, and we call the relationship type that relates a weak entity type to its owner the <b>identifying relationship</b> of the weak entity type.

A weak entity type always has a <i>total participation constraint</i> (existence dependency) with respect to its identifying relationship because a weak entity cannot be identified without an owner entity. However, not every existence dependency results in a weak entity type.

## 3.6 Refining the ER Design for the Compnay Database

## 3.7 ER Diagram, Naming Conventions, and Design Issues

### 3.7.1 Summary of Notation for ER Diagrams

### 3.7.2 Proper Naming of Schema Constructs

### 3.7.3 Design Choices for ER Conceptual Design

### 3.7.4 Alternative Notations for ER Diagrams

## 3.8 Example of Other Notation: UML Class Diagrams

## 3.9 Relationship Types of Degree Higher than Two

### 3.9.1 Choosing between Bianry and Ternary (or Higher-Degree) Relationships

### 3.9.2 Constraints on Ternary (or Higher-Degree) Relationships

### 3.10 Another Example: a university database

## 3.11 Summary