# What is DFRNT.tech (BETA)

DFRNT.tech is a client to TerminusX data products. Two main features are implemented: 

* Visualisation of documents and document dependencies
* Data modelling

To dive deep in to TerminusDB, consider using their documentation, it is highly recommended: [https://terminusdb.com/docs/](https://terminusdb.com/docs/). Most questions on how to model documents in DFRNT.tech is likely answered there.

The current DFRNT.tech implementation is the data modelling backend for the upcoming changemaker tools.

## Visualisation of documents and document dependencies

Records and their interdependencies through records linking are visualised using the Canvas section. By searching for, or browsing the data model, records are added to the Canvas. Any connections between them are visualized using directional links primarily through an acyclic directed graph. Cycles in the graph are supported but does not always render great graphs.

### Canvas

Inbound and outbound linked records can be added through the menu available through clicking on each record.

The canvas can be exported to PNG by clicking the canvas, which is also how to clear the canvas.

### Render and browse records as Markdown documents

Document contents can be viewed by opening a record through the canvas, or by browsing for records through the Data Model.

`Markdown` traits (with a mandatory or optional string field called `markdown`) will be rendered as markdown text, useful for making nodes browseable and contain lengthier texts. Pictures are not supported, but may be possible to use through data: elements for the brave.

By using `Markdown` documents and use markdown links, documents can be made browseable like a Wiki, using relative links such as `../Type/documentId`, with the ids that can be copied using the clipboard icon in the user interface.

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
