# system design for law students

need to design a system a case to handle a specific law regarding the nature of the state of health

somehow, this in turn leads to a law for abortion rights if the lawyer is so inclined to pursue it.

### three questions arise

how do laws relate and work

why do they work that way

implement a law for this

### relational properties between two laws

Example System

```cypher
CREATE
(law1:Law { name: 'Law 1', subject: 'health'}),
(law2:Law { name: 'Law 2', subject:'health'}),
(law3:Law {name: 'Law 3', subject: 'medications'}),
(law1)-[:RELATED_TO]->(law2),(law2)-[:RELATED_TO]->(law1),
(law2)-[:RELATED_TO]->(law3)
```

```cypher
MATCH(law:Law)-[:RELATED_TO]-(health) WHERE law.subject = 'health' return law,health
```

### Cases

5150

5585

Arlen

### References

Furrow, B. R., Greaney, T. L., Johnson, S. H., Jost, T. S., Schwartz, R. L., Clark, B. R., Fuse Brown, E. C., Gatter, R., & King, J. S. (2018). Health law: Cases, materials, and Problems. West Academic Publishing. 
