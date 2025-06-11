# Some examples from the slides

## Information in XML 
`person.xsd` contains an example XML Schema and `person.xml` contains some instance data that conforms to that schema

In order to validate using the command line, it is possible to use: `xmllint`

```sh
xmllint --schema person.xsd person.xml --noout
```

## Information in RDF

- `person.ttl` contains the RDF example from the slides in RDF (Turtle format)

Using `rudof`, it is possible to check that it is well formed with:

```sh
rudof data person.ttl
```

It is also possible to ask for information about a node using:

```sh
rudof node -n :timbl person.ttl
```

- `person.sparql` contains an example SPARQL query 

It is possible to run the SPARQL query using:

```sh
rudof query -q person.sparql person.ttl
```

- `person_checkname.sparql` is a SPARQL query that checks that a person has exactly one name of type `xsd:string` and one birth date which should be of type `xsd:date`.