# ContentDB

A document store (or [document-oriented database](https://en.wikipedia.org/wiki/Document-oriented_database), like "NoSQL" (not table-oriented) variants - [CouchDB](https://en.wikipedia.org/wiki/Apache_CouchDB) and [MongoDB](https://en.wikipedia.org/wiki/MongoDB)) that uses a [file](https://en.wikipedia.org/wiki/Computer_file) to store each record.  This is similar to [RDF](https://en.wikipedia.org/wiki/Resource_Description_Framework)-style [XML databases](https://en.wikipedia.org/wiki/XML_database).

Using this approach, you have the power of easy-to-manage data storage, retreival, and relating.  And, you can easily do version control for history tracking and easy deployment.

To massively improve performance and scalability, [Tantivy](https://github.com/tantivy-search/tantivy) integration can provide immediate indexing and querying.

The current version is in Lua.  See [ContentDB-Lua](https://github.com/foundpatterns/contentdb-lua).

## Format

ContentDB mixes structured and unstructured data formats.  The header uses the [SCL](https://github.com/Keats/scl) data format, and the body uses the [Markdown](https://en.wikipedia.org/wiki/Markdown) markup format.

Fields have Values.  Relationships use the target's model for its field.

UUIDv4 is the default id.  Short names are a missing feature.
