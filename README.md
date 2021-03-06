## pyNIF-lib

## What is NIF (NLP Interchange Format) ?

The NLP Interchange Format (NIF) is an RDF/OWL-based format that aims to achieve interoperability between Natural Language Processing (NLP) tools, language resources and annotations. NIF consists of specifications, ontologies and software (overview).

## Documentation

[NIF Documentation](http://persistence.uni-leipzig.org/nlp2rdf/)


## Supported versions

 * 2.1

## Supported formats

* Turtle

## Usage

0) Import and instantiate

```
import NIF21


nif21 = NIF21.NIF21()

```

1) Create a context

```
nif21.context("http://freme-project.eu", 0, 33, "Diego Maradona is from Argentina.")

```

2) Create entries for the entities

```
nif21.bean('Diego Maradona',
           0,
           14,
           ['http://dbpedia.org/ontology/SportsManager', 'http://dbpedia.org/ontology/Person', 'http://nerd.eurecom.fr/ontology#Person'],
           0.9869992701528016,
           'http://freme-project.eu/tools/freme-ner',
           'http://dbpedia.org/resource/Diego_Maradona',
           'http://dbpedia.org/ontology/SoccerManager')


nif21.bean('Argentina',
           23,
           32,
           ['http://dbpedia.org/ontology/PopulatedPlace', 'http://nerd.eurecom.fr/ontology#Location',
            'http://dbpedia.org/ontology/Place'],
           0.9804963628413852,
           'http://freme-project.eu/tools/freme-ner',
           'http://dbpedia.org/resource/Argentina',
           None)
```

3) Finally, get the output with the format that you need

```
print nif21.turtle()
```


## Issues

If you have any problems with or questions about this library, please contact us through a [GitHub issue](https://github.com/NLP2RDF/pyNIF-lib/issues).

## Maintainers

<a href="http://infai.org"><img src="http://infai.org/de/Presse/Logos/files?get=infai_logo_en_rgb_300dpi.jpg" align="left" height="20%" width="20%" ></a>
