## Polifonia KG Line lyric-specific Similarity ETL

Here you find code to produce Polifonia KG line lyric specific related triples.

For the mapping from raw data to RDF is used [sparql.anything](https://github.com/SPARQL-Anything/sparql.anything).
Please see relative project site for installation and configuration.

Running: `fx -q queries/linelyric.sparql` will output the KG in the console.


To output a version of the knowledge graph in `kg/versions` folder run:

```fx -q queries/linelyric.sparql -f TTL -o kg/versions/polifonia-kg-linelyric-{MAJOR.MINOR.PATCH}.ttl```

e.g. ```fx -q queries/linelyric.sparql -f TTL -o kg/versions/polifonia-kg-linelyric-0.0.1.ttl```



To update the latest version of the knowledge graph in `kg/` folder run:

```fx -q queries/linelyric.sparql -f TTL -o kg/polifonia-kg-linelyric-latest.ttl```


### Tutorial

```fx -q queries/tutorial.sparql -f JSON -o kg/tutorial/tutorial.jsonld```

