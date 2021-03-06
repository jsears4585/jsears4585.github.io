## Mongo DB

### History

MongoDB was founded in 2007 by previous members of the DoubleClick team, an internet advertising company that has since been bought-out by Google. MongoDB was open sourced in 2009, and the company now sells support and additional services, such as Atlas, Stitch and MongoDB Cloud Manager.

![mongodb companies](http://cdn.jsears.co/mongodb-companies.png "Mongo DB Companies Served")

### Benefits of NoSQL vs. Relational Database Management Systems (RDBMS)

It should first be made clear that NoSQL isn't meant to replace or phase out traditional RDBMS, but to instead add to the functionality companies like Oracle have been helping to develop over the past 40 years. That being said, the way in which NoSQL databases like MongoDB are set up offer some very helpful ways of dealing with data.

* schemaless structure
* no complex joins
* structure of a single document is clear (few foreign keys)
* powerful query language
* easy to scale (or shard)
* replication and high-availability

### Analogies between NoSQL and traditional RDBMS

![mongodb-v-relational](http://cdn.jsears.co/mongo-vs-rdbms.png "Mongo v. Relational Keywords")

### But What Does 'Schemaless' Mean, Exactly?

Data stored inside of a MongoDB database is represented in JSON-style documents. Each of these documents can have a varying set of fields, with a variety of data types. Instead of relying on unique and foreign key matching, a json-like (BSON) data structure in MongoDB typically contains all of the data relevant to that particular document. This means fewer complex joins and easier horizontal scaling.

![mongo document model](http://cdn.jsears.co/document-model.png "Mongo Document Model")

In the image above, you'll notice that (in this case) joins are not necessary because all of the relevant information is nested inside one document.

It's also important to recognize that MongoDB databases make schema migrations easy since there are no migration to write or rollback. In MongoDB, adjustments to the structure of the database are transparent and immediate. A field can be added to a document when necessary, and if that field is requested later on a document that doesn't contain that it, the query will simply return null.

### More on the Document Model

![potential relational setup](http://cdn.jsears.co/db_schema_rel.png "Potential Relational Setup")

Above is an example of a traditional RDBMS setup for a movie application. Below, I've included an example for a single movie document from a NoSQL-type database.

![mongo document model details](http://cdn.jsears.co/Document%20Example.png "Mongo Document Model Details")

You'll notice above that mostly all of the relevant details for the movie "A Good Day to Die Hard" are included in a single document, including mulitple nested objects. This architecture limits the amount of required joins and may very well provide scalability and permformance advantages as well, depending on the particular use case. This design only requires a single read from memory or disk, whereas RDBMS often require multiple reads from multiple locations.

I'll be creating additional MongoDB posts in the future, so please let me know if there's anything I can try to help address. Thanks for reading!
