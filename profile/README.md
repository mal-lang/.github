## Welcome to the home of the Meta Attack Language (MAL)

### What is MAL?
MAL is a language for creating domain-specific threat modeling languages - a malLang. MAL could be thought of as a framework for combining systems modeling such as UML with attack graphs. More precisely, MAL formalizes how to generate attack graphs from system model specifications. In a malLang you specify Asset categories (e.g. computers, applications, networks, data), how they are allowed to be related (e.g. computers can run applications and be connectedTo networks), what attack actions are possible to perform on the respective Assets (e.g. we can connect, authenticate, guessCredentials, and compromise computers) as well as which successful attack action would enable attempting new actions (e.g. after succeeding to connect to a computer you can either authenticate -if you have credentials- or guess the credentials. If either of these actions are successful you will have compromised the computer and you will be able to connect to all other computers located on the same network as the compromised computer.) Depending on how system assets are configured in an instance model -what the system architecture look like- this will thus determine what attack vectors are possible according to the domain-specific language and express them in an attack graph.

### Why MAL?
With MAL it is possible to encode cybersecurity competence so that it can be reused for many system environments. Cybersecurity experts can describe how systems can be attacked and also defended, and this knowledge can be applied by system designers and maintainers for analyzing their particular system environment. MAL thus enables the construction of a digital twin for cybersecurity in which red team simulations can be made at scale. In addition, the effect of blue team interventions can be studied. This can be used for traditional threat modeling and security analysis identifying effective security design, but also for operations guiding protective actions given the observation of some particular attack chain. Moreover, the MAL asset graphs and attack graphs can also be used as a simulation infrastructure for simulation-based training of attacker and defender agents, for instance through machine learning.

### MAL resources
MAL has been developed by Software Systems Architecture and Security group [[1]](https://www.kth.se/cs/nse/research/software-systems-architecture-and-security) [[2]](https://github.com/KTH-SSAS) at KTH Royal Institute of Technology in Sweden and this organization gathers results of many of the various projects that the research group has been working on over the years. A few highlights of these are:

#### MAL documentation

- [MAL Documentation wiki](https://github.com/mal-lang/mal-documentation/wiki) to learn how MAL languages are built

- [MAL toolbox documentation](https://mal-lang.org/mal-toolbox/)

- [MAL toolbox tutorial](https://github.com/mal-lang/mal-toolbox-tutorial) to learn how the MAL tools work.

#### MAL Tools

- The [MAL Toolbox](https://github.com/mal-lang/mal-toolbox), which contains support for building asset instance models from a given MAL language and then generating the corresponding attack graph from the asset instance model.

- The [MAL Simulator](https://github.com/mal-lang/mal-simulator), which is an infrastructure for using the MAL attack graphs as a game board where defender and attacker agents can “play” against each other. It can be used as a simulator for machine learning of the agents.
  - Find example simulator scenarios in the [malsim-scenarios repository](https://github.com/mal-lang/malsim-scenarios).

- The [MAL-GUI](https://github.com/mal-lang/mal-gui), which is a super simple drag-n-drop studio for creating instance models given some chosen MAL-language. (However, it does not support visualization for attack graphs, for that we recommend Neo4j - see the MAL Toolbox documentation.)

- The [mal-vs-code-extension](https://github.com/mal-lang/mal-vscode-extension) for MAL language support in VS Code. Depends on [mal-language-server](https://github.com/mal-lang/mal-ls) which builds on the [MAL tree sitter grammar](https://github.com/mal-lang/tree-sitter-mal).

#### MAL Languages

- [exampleLang](https://github.com/mal-lang/exampleLang/blob/master/src/main/mal/exampleLang.mal), which is a language devised to demonstrate how MAL works and good to start with if you are new to MAL.

- [coreLang](https://github.com/mal-lang/coreLang), which is a language that has the ambition to cover the most common attack vectors found in common IT environments.

- [tyrLang](https://github.com/mal-lang/tyrLang), a simpler variant of coreLang built for an external project.


#### Academic papers
More academic papers related to various MAL projects have been produced than what can be mentioned here, but there exist two papers on MAL per se:
- Pontus Johnson, Robert Lagerström, and Mathias Ekstedt. 2018. A Meta Language for Threat Modeling and Attack Simulations. In Proceedings of the 13th International Conference on Availability, Reliability and Security (ARES '18). Association for Computing Machinery, New York, NY, USA, Article 38, 1–8. https://doi.org/10.1145/3230833.3232799
- Wojciech Wideł, Simon Hacks, Mathias Ekstedt, Pontus Johnson, Robert Lagerström, The meta attack language - a formal description, Computers & Security, Volume 130, 2023, 103284, ISSN 0167-4048, https://doi.org/10.1016/j.cose.2023.103284

#### ..And more
Also check out our sister project, [DynaMAL](https://gitlab.com/kth-ssas/dynamal-group/dynamal-documentation), featuring logic to update the asset and attack graphs dynamically during simulations, based on attacker actions.
