# ContentDB

`contentdb` is a database library implemented for Torchbear to act as a document store, aka a [document-oriented database](https://en.wikipedia.org/wiki/Document-oriented_database), like "NoSQL" databases (also usually document-oriented, or otherwise graph-oriented, not table-oriented), [CouchDB](https://en.wikipedia.org/wiki/Apache_CouchDB) and [MongoDB](https://en.wikipedia.org/wiki/MongoDB)).

we makes it significantly different is that it uses a [file](https://en.wikipedia.org/wiki/Computer_file) to store each "record", called a document.  This is similar to [RDF](https://en.wikipedia.org/wiki/Resource_Description_Framework)-style [XML databases](https://en.wikipedia.org/wiki/XML_database).

This approach gives you easy-to-manage data storage, retreival, and relation-field and other metadata storage and retrieval, add well.  Also, you can easily do version control for history tracking and easy deployment.

To massively improve performance and scalability, [Tantivy](https://github.com/tantivy-search/tantivy) integration can provide immediate indexing and querying.

The current version is in Lua.  See [ContentDB-Lua](https://github.com/foundpatterns/contentdb-lua).

## Format

ContentDB mixes structured and unstructured data formats.  The header uses the [SCL](https://github.com/Keats/scl) data format, and the body uses the [Markdown](https://en.wikipedia.org/wiki/Markdown) markup format.

Fields have Values.  Relationships use the target's model for its field.

UUIDv4 is the default id.  Short names are a missing feature.
