---
id: data-modeling
title: Data Modeling
permalink: guides/couchbase-lite/native-api/data-modeling/index.html
---

If you’re familiar with data modeling for relational databases, you'll notice differences in the way it is done for Couchbase Lite.

Couchbase Lite is a document database. Unlike traditional relational databases, data is stored in documents rather than in table rows. A document is a JSON object containing a number of key-value pairs. Entities, and relationships between entities, are managed within the document itself.

## The Basics

A starting point for data modeling in Couchbase Lite is to look at a denormalized entity stored in a single document. Consider modeling a contact record stored in a relational database in a CONTACTS table, of the form:

|ID|FIRST_NAME|LAST_NAME|EMAIL|
|:--|:---------|:--------|:----|
|100|John|Smith|john.smith@couchbase.com|

The equivalent representation in JSON document form would be something like:

```javascript
{
   "id": "contact100",
   "type": "contact",
   "first_name":"John",
   "last_name ":"Smith",
   "email": "john.smith@couchbase.com"
}
```

Functionally related properties can be grouped using an embedded document. If we wanted to store address information for our contact, it could be modeled as:

```javascript
{
   "id": "contact100",
   "type": "contact",
   "first_name": "John",
   "last_name ": "Smith",
   "email": "john.smith@couchbase.com",
   "address": {
      "address_line": "123 Main Street",
      "city": "Mountain View",
      "country": "US"
   }
}
```

## One-to-Many Relationships

Things get interesting when the contact record has more than one related record that we want to model. There are two main options for modeling one-to-many relationships in a document database - as embedded documents, and as related documents.

### Using Embedded Documents

When a contact can have more than one address, the addresses would commonly be stored in a relational database using a separate ADDRESSES table:

|ID|CONTACT_ID|ADDRESS_LINE|CITY|COUNTRY|
|:--|:---------|:-----------|:---|:------|
|200|100|123 Main Street|Mountain View|US|
|201|100|123 Market|San Francisco|US|

In a document database, the address information could instead be stored as an array of embedded documents within the contact document:

```javascript
{
   "id": "contact100",
   "type": "contact",
   "first_name": "John",
   "last_name" : "Smith",
   "email": "john.smith@couchbase.com",
   "addresses": [
    {
      "address_line": "123 Main Street",
      "city": "Mountain View",
      "country": "US"
    },
    {
      "address_line": "123 Market",
      "city": "San Francisco",
      "country": "US"
    }
   ]
}
```

The embedded document approach reduces the amount of work that your application needs to do in order to work with the Contact object – there is no additional query required to retrieve the embedded information.

### Using Related Documents

There are scenarios where the embedded document approach isn’t ideal, including:

- _Large number of related entities._ Embedding a large number of related entities results in a large document. This can result in slower document handling, as the entire document needs to be passed around when making updates.
- _Concurrency._ When multiple users are working on a single document, there’s a higher risk of conflicts being introduced. Related documents can be used to isolate updates being made by different users.

The most common implementation for related documents is the belongsTo pattern. Consider the scenario where any user can assign a task to a contact, and a contact can end up with a large number of volatile task records. Here we define a new task document, which includes the contact key that the task record belongs to:

```javascript
{
  "id": "task300",
  "type": "task",
  "contact_id": "contact100"
  "description": "Task details",
  "status": "complete"
}
```

Under this implementation, users can modify task records concurrently without introducing conflict scenarios for the related contact record. It can also support a large number of task records per contact without impacting the size of the related contact record.