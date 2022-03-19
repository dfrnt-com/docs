# What is DFRNT.tech

DFRNT.tech is a client to TerminusX data products. Two main features are implemented: Data modelling and visualisation of document dependencies, it is a technical version of the upcoming tools for changemakers.

## Data modelling

The data modelling capabilities of DFRNT.tech involves five categories of data structures: Records, Properties, Types, Traits and Enums.

### Records

Records is where data lives. Records may include the following kinds of properties (data fields):

* **Base types** (strings, numeric, geographical, time, etc.)
* **Links to other records of a type** (documents in TerminusDB)
* **Enum constants** (enum in TerminusDB)
* **Traits** (subdocuments in TerminusDB)

### Properties

Properties hold the data and references in the system. Beneath the data model, it's RDF triples all the way down, but constrained by a schema checker that checks that all data is consistent.

The properties on Types and Traits can either be of a base type or link to other Types, Traits or Enum values and data structures. Base data properties, Traits and Enums are attached directly to the Record, while Type references are directional links to other records.

Composition of Traits and Types means that property definitions from their parents get inherited. The same property name may not be inherited from multiple parents.

### Types

All records have a type that defines the data structure of the record. Types have properties that may be composed (inherited) from one or multiple types.

### Traits

Traits are reusable data structures that can be attached to types as properties, and may be composed by one or multiple traits. By defining a data structure as a trait, instead of as a type, it can be reused across types to build complex data structures.

Some traits have special meaning in DFRNT.tech and are used to build data structures and taxonomies that have semantic meaning, as part of the collaborative semantic knowledge graph.

### Enum constants

Enumerations (list of constant values) can be used to constrain properties to certain values. They are frequently used for categories and other sets of information.
