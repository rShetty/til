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

### MySQL Query Optimization

- Try to compare columns that have the same data type.
- Try to make indexed columns stand alone in comparison expressions.
- Don't use wildcards at the beginning of a LIKE pattern.
  (Note: REGEXPexpressions are never optimized)
- Help the optimizer make better estimates about index effectiveness.
- Use EXPLAIN to verify optimizer operation.
- Give the optimizer hints when necessary.
- Take advantage of areas in which the optimizer is more mature( "Rewriting Subqueries as Joins).
- Avoid overuse of MySQL's automatic type conversion.

