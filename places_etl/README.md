## Polifonia KG Places ETL

Here you find code to produce Polifonia KG places related triples.

For the mapping from raw data to RDF is used [sparql.anything](https://github.com/SPARQL-Anything/sparql.anything).
Please see relative project site for installation and configuration.

Running: `fx -q queries/places-latest.sparql` will output the KG in the console.


To output a version of the knowledge graph in `kg/versions` folder run:

```fx -q queries/places-latest.sparql -f TTL -o kg/versions/polifonia-kg-places-{MAJOR.MINOR.PATCH}.ttl```

e.g. ```fx -q queries/places-latest.sparql -f TTL -o kg/versions/polifonia-kg-places-0.0.1.ttl```



To update the latest version of the knowledge graph in `kg/` folder run:

```fx -q queries/places-latest.sparql -f TTL -o kg/polifonia-kg-places-latest.ttl```


### Tutorial

A tutorial for sparql.anything

```fx -q queries/raw-data/tutorial.sparql -f JSON -o kg/tutorial/tutorial.jsonld```

