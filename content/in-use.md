## In-use
{:#in-use}

To further help people get started with Comunica we have provided tutorials on multiple conferences
which help with some of the first hurdles in getting everything working and making use of it.
These [tutorials](https://comunica.github.io/Tutorial-ESWC2019-Comunica/) can all be found online 
and give a solid introduction to getting started with Comunica.
These can be used next to the existing documentation to fully grasp what can be done with the system
and how it can be extended.

The [first](https://github.com/comunica/Tutorial-Comunica-Querying-Data/) tutorial
covers all the different ways the already existing actors and configurations can be used
to execute SPARQL queries over new and existing data sources.
These range from executing queries with a command line tool
to embedding Comunica in the code of your own project
to setting up a Web service other users can use to execute queries.

The [second](https://github.com/comunica/Tutorial-Comunica-Reduced-Actor/) tutorial
explains all the steps necessary to create a new actor that can be embedded into the existing configurations.
This includes an overview of all the configuration files that are required
and what each of them has to contain.
Besides that it also covers the helper classes that can be used
and how an existing configuration can be adapted to add the new actor.

[LDflex](https://github.com/RubenVerborgh/LDflex) is a language that allows developers
to easily access RDF data in JavaScript.
This makes RDF data much more accessible for front-end developers and other people who might not be used
to working with SPARQL queries but still want to make use of Linked Data,
thereby making it easier to spread the use of Semantic technologies.
It is used by the [Solid client](https://github.com/solid/query-ldflex) among other,
and to support queries it makes use of [Comunica](https://github.com/RubenVerborgh/LDflex-Comunica).
Additionally, a Comunica [actor](https://github.com/comunica/actor-http-solid-auth-fetch)
has already been made to support making HTTP requests using Solid authentication,
allowing users to query their private Solid data through Comunica.

[Sparqlee](https://github.com/comunica/sparqlee){:.mandatory}
is a JavaScript library to evaluate SPARQL expressions.
This library was built for Comunica to support these expressions,
but due to the modular nature of Comunica,
it can also fully stand on its own as a separate library
and could even be used by other SPARQL libraries to handle their expressions.

The Comunica [repository](https://github.com/comunica/comunica) already has been starred 89 times
at the time of writing and has been forked 12 times.
The core Comunica npm [package](https://www.npmjs.com/package/@comunica/core),
which is required for all Comunica variants,
currently has 1083 weekly downloads.
All Comunica packages can also be found separately on [npm](https://www.npmjs.com/org/comunica).
Currently there are already 128 packages available to be used.
