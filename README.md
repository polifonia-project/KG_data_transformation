# Polifonia KG transformations

Script and services to extract data from raw files JSON, csv, tsv and create Polifonia KG.

In this repository we collect datasets and data populating polifonia KG.


Data are modelled according to the [Polifonia Ontology Network](https://github.com/polifonia-project/ON)

Latest version of the [Polifonia KG](https://github.com/polifonia-project/kg_sparql_endpoint) deployable with docker is available.


Data populating the KG are:

- [places](places_etl/kg/polifonia-kg-places-latest.ttl)
- [harmonic similarity](harmonic_sim_etl/kg/polifonia-kg-harmonic-sim-latest.ttl)

Transformation producing RDF are:

- [places transformation](places_etl/queries/places-latest.sparql)
- [harmonic sim transformation](harmonic_sim_etl/queries/harmonic-similarity-latest.sparql)


## Dev

To create a transformation for new data create a folder with following tree at the root of this project.

```
my_transformation_etl
    | _ data
    |   |_ mydata.{csv,json,...}
    |
    | _ kg
    |   |_ my-transformation-kg-latest.ttl
    |
    | - queries
        |_ my-transformation-latest.sparql
```

Be sure that at least a `{my-transformation}-latest.ttl` and `{my-ouput-kg}-latest.ttl` is presented at the specified paths.
[Polifonia KG Sparql Endpoint](https://github.com/polifonia-project/kg_sparql_endpoint) will point to these locations while harvesting data.


### Test

You can manually test latest versions of KG if you have [kgdd](https://github.com/ccolonna/kgdd) installed with following commands:

`kgdd -t ./places_etl/kg/test/testbed-latest.json -f ./places_etl/kg/polifonia-kg-places-latest.ttl`

`kgdd -t ./harmonic_sim_etl/kg/test/testbed-latest.json -f ./harmonic_sim_etl/kg/polifonia-kg-harmonic-sim-latest.ttl`


