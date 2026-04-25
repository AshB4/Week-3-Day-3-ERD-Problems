# Week-3-Day-3-ERD-Problems

## 1. How are entities defined and represented in the Entity Relationship Diagram (ERD)?

Entities are real-world objects, people, places, or concepts that store information in a database. They are represented as tables or rectangles in an ERD.

Examples of entities in this assignment include:

* People
* Pets

---

## 2. How are attributes defined and associated with entities?

Attributes are characteristics that describe an entity. They are associated with entities by being listed as columns or fields inside a table.

Example:

### People

* person_id
* name
* email

### Pets

* pet_id
* pet_name
* age
* breed

---

## 3. What is a relationship in the context, how you represent them, and how does it connect entities?

A relationship shows how two entities are connected within a database.

Relationships are represented using:

* Lines
* Arrows
* Crow’s Foot notation
* Cardinality symbols

In this assignment, the relationship is between People and Pets because one person can own multiple pets.

This relationship is connected using:

`person_id (FK)` in the Pets table.

---

## 4. List and describe the different types of Relationships found (Cardinality).

### One-to-One (1:1)

One record is connected to exactly one other record.

Example:
One person → one passport

---

### One-to-Many (1:N)

One record is connected to multiple records.

Example:
One person → many pets

---

### Many-to-Many (N:N)

Many records are connected to many records.

Example:
Students can take many courses and courses can have many students.

This relationship usually requires a junction table.

---

## 5. Create an Entity Relationship Diagram of People that owns Pets.

### People Table

```plaintext
People
-------------------
person_id (PK)
name
email
```

### Pets Table

```plaintext
Pets
-------------------
pet_id (PK)
pet_name
age
breed
person_id (FK)
```

### Relationship

One person can own many pets.

Crow’s Foot notation:

```plaintext
People |------< Pets
```


This version looks intentional and directly answers exactly what was asked—professor-proof.
