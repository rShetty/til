## MySQL Query Optimization

### Benefits of Indexing 

- Faster Lookups.

### Costs of Indexing

- Slows down Insertions/Updations/Deletions.
- Disk Space.

### Choosing Indexes

- Index columns that you use for searching, sorting, or grouping, not columns you only display as output.
- Consider column cardinality.
- Index prefixes of string values.
- Take advantage of leftmost prefixes.
- Don't over-index.
- Match index types to the type of comparisons you perform. (Hash based/ B-tree indexing).

