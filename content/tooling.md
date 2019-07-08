## Tooling
{:#tooling}

There are already several tools available to further extend what can be done with Comunica
or to help in its usage.

### jQuery Widget
The [jQuery Widget](https://github.com/comunica/jQuery-Widget.js/){:.mandatory}
creates a browser-based GUI for the Comunica SPARQL client,
allowing users to execute SPARQL queries in their browser without having to install anything.
While it originally made use of the TPF client,
and thus had less support for heterogeneous sources,
it now uses Comunica in the backend providing all its advantages.
Besides the support for many different kinds of interfaces,
it also supports executing GraphQL queries over those sources.
Changing the Comunica configuration that is being used
is simply a question of changing the configuration file in the repository,
thereby allowing anyone to quickly set up an online querying engine with their own implementation.

### Bencher
Although evaluations are much easier with Comunica due to the easy swapping of modules,
there is still some work that needs to be done before they can actually happen,
such as setting up the server, adding the test data and having test queries.
[Comunica bencher](https://github.com/comunica/comunica-bencher/){:.mandatory}
helps users skip several of those steps.
It can automatically generate everything that is necessary to set up a TPF server,
create a [Watdiv](cite:cites watdiv) dataset and corresponding queries.
It can then also set up a client to run those queries over the server
and generate graphs from the results.
Although not every kind of setup can be covered with this,
it is already incredibly useful for many use cases.
Specifics such as the amount of dry runs, caching, data size, etc.
can all be tweaked in the configuration,
allowing users to fine-tune the tool to their needs.
Finally, this way the tests can also easily be shared for later reuse.

### Generator
Creating a Comunica actor can be a complex endeavour for developers without any experience in the system:
several configuration files have to be made,
these have to be mapped to the code,
and the code has to be follow certain rules to make sure it integrates with the rest of Comunica.
That is why we created a [Comunica generator](https://github.com/comunica/generate-comunica){:.mandatory},
which creates an empty actor with all the necessary files already in place with all the default values.
It creates this initial project by asking the user several questions
and then automatically generates the corresponding TypeScript and JSON-LD files
with the values based on the answers.
These still need to be changed, especially if the user has many extra requirements for their actor,
but it greatly reduces the start-up time when coding and reduces the chances of errors or missing files.
