---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
# transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 35min
---

# Entity Relationship Design

CST 363


---

## Recap: Course Outline

- SQL
  - How to use a relational DB?
- Database implementation
  - How do relational DBs work?
- Database design
  - How to design a database schema?
- Beyond relational databases 


---

## Problem Statement

Suppose someone asks you to model data for their business or organization
Problems:

- Where do you even begin?
- Who has the information? Who are the stakeholders?
- Should you write a relational schema right away?
- How to avoid need for big changes in future?
- How to share your model with others?


---

## What is a good first model?

Some things we might want:

- Uses simple, everyday concepts
- General — can map onto various detailed models
- Is easy for non-experts to understand
- Can be presented as a picture
- Ties closely to elements of a human language
- Provides a conceptual framework for later work


Is a programming language a good first modeling language?

How about English?



---


## Phases of the database design process

- Understand data needs of future users
  - Talk to users and domain experts; write things down
- Create a conceptual design
  - identify objects, their relationships, etc.
  - ER model
- Identify functional requirements
  - What will users do with the data?
- Logical and physical design
  - Map conceptual design to data model
  - Specify physical features of DB, like file organization



---


## Entity-Relationship (ER) Models

- Developed by Peter Chen of MIT
- Used for conceptual design
- Building blocks of ER model
  - entities
  - relationships
  - attributes


We’ll use a digital music library as our running example

---


<img src="/images/chen-er.png" class="w-150" />



---

## Inspiration from Chinese character development 


<img src="/images/chinese.png" class="w-150" />



---

## Inspiration from Egyptian Hieroglyphs

<div class="p-5">


<img src="/images/egyptian.png" class="w-100" />


</div>

---

## Example ER Model – Chen-style attributes


<img src="/images/chen-d1.png" class="w-100" />


- entities represented as rectangles
- attributes represented as ovals, primary key is underlined
- relationships represented as diamonds (not shown here)


---

## Example ER Model — Hybrid variant


<img src="/images/hybrid.png" class="w-100" />




- here, “contribution” (diamond) is a relationship
- “contribution” is shown to have two attributes


---


## Entities and entity sets


- Entity
  - A real-world thing that is distinguishable from others
  - It has a set of properties, or attributes
  - Can be physical (book) or abstract (course section)
  - What are some music library examples?
- Entity set
  - A collection of similar entities
  - Example: “instructor” is the collection of people at a 
  - university that share some properties
  - What are some music library examples?




---

## Attributes


- Similar to object-oriented prog. languages
- Each entity has a value for each of its attributes
- ‘Instructor’ attributes could include ID, name, salary, etc.
- Example: instructor has value “Wu” for name


In music library, what might be attributes of:
- artist?
- track?
- album?


---

## Entity sets and attributes for music library

- Let’s think of entity sets for the music library
- Let’s think of attributes for these entity sets


---

## Relationships and relationship sets

- Relationship
  - An association between entities
  - For example, student Shankar is 
  - advised by instructor Gold
  - A relationship can involve 2 or 
  - more entities
- Relationship set
  - A collection of relationships of the 
  - same type
  - For example, ‘teaches’ and ‘takes’ are 
  - relationship sets


---

## More on relationship sets

- Participation
  - ‘instructor’ participates in the ‘teaches’ relationship set
  - ‘student’ participates in the ‘takes’ relationship set
- Roles
  - this is useful in relationship sets like ‘prerequisite’, where the same entity set appears more than once
  - example: “parent-of” relationship between people
- Attributes of relationships
  - ‘advisor’ relationship has a date when advising began
  - ‘takes’ relationship has a grade attribute


---

## Relationship sets for music library


- Let’s try to think of relationship sets for the music library


---

## More on attributes


- Every attribute has a domain of permitted values
  - like a type in a programming language
- Attributes can be simple or composite
  - simple: age, salary
  - composite: date, address
- Attributes can be multi-valued
  - example: my contact phone numbers
- Attributes can take value ‘null’


---

## Attributes for music library?


---

## ER vs OO modeling


- Similar concepts used:
  - entity sets ~ classes
  - entities ~ instances
  - attributes ~ attributes
  - relationships not explicit in OO models
  - inheritance "sort of" modeled in ER (“is-a relationship”)
- Which is better?
  - one experimental study says ER is a little better
  - ER models faster to develop; preferred by modelers


---

## Summary

- Database design
  - conceptual design
  - functional requirements
  - logical and physical design
- ER models are for conceptual design
- Concepts in an ER model:
  - entities, entity sets
  - relationships, relationship sets



