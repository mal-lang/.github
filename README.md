## Welcome to the home of the Meta Attack Language (MAL)

### What is MAL?
MAL is a language for creating for creating domain-specific threat modeling languages - a malLang. MAL could be thought of as a framework for combining systems modeling such as UML with attack graphs. More precisely, MAL formalizes how to generate attack graphs from system model specifications. In a malLang you specify Asset categories (e.g. computers, applications, networks, data), how they are allowed to be related (e.g. computers can run applications and be connectedTo networks), what attack actions that are possible to perform on the respective Assets (e.g. we can connect, authenticate, guessCredentials, and compromise computers) as well as what successful attack action would enable attempting new actions (e.g. after succeeding to connect to a computer you can either authenticate -if you have credentials- or guess the credentials. If either of these actions are successful you will have compromised the computer and you will be able to connect to all other computers located on the same network as the compromised computer.) Depending on how system assets are configured in an instance model -what the system architecture look like- this will thus determine what attack vectors are possible according to the domain-specific language and express them in an attack graph. A documentation wiki is found here: https://github.com/mal-lang/mal-documentation/wiki

### Why MAL?
With MAL it is possible to encode cybersecurity competence so that it can be reused for many system environments. Cybersecurity experts can describe how systems can be attacked and also defended, and this knowledge can be applied by system designers and maintainers for analyzing their particular system environment. MAL thus enables the construction of a digital twin for cybersecurity in which red team simulations can be made at scale. In addition the effect of blue team interventions can be studied. This can be used for traditional threat modeling and security analysis identifying effective security design, but also for operations guiding protective actions given the observation of some particular attack chain. Moreover, the MAL asset graphs and attack graphs can also be used as a simulation infrastructure for simulation-based training of attacker and defender agents, for instance through machine learning.

### MAL resources
MAL has been developed by Software Systems Architecture and Security group at KTH Royal Institute of Technology in Sweden and this repo gathers results of many of the various projects that the research group has been working on over the years. A few highlights of these are:
- The MAL Toolbox that contains support for building asset instance models from a given MAL language and then generating the corresponding attack graph from the asset instance model. Documentation can be found here. https://mal-lang.org/mal-toolbox/index.html 
- exampleLang, which is a language devised to illustrate how MAL works. A good place to start if you are new to MAL.
- coreLang, which is a language that have the ambition to cover the most common attack vectors found in common IT environments.
- MAL-GUI, which is a super simple drag-n-drop studio for creating instance models given some chosen MAL-language. (However, it does not support visualization for attack graphs, for that we recommend Neo4j - see the MAL Toolbox documentation.)
- MAL simulator, which is infrastructure for using the MAL attack graphs as game board where defender and attacker agents can “play” each other. It can used as a simulator for machine learning of the agents. 

### Academic papers
More academic papers related to various MAL projects have been produced than what can be mentioned here, but there exist two papers on MAL per se: 
- Pontus Johnson, Robert Lagerström, and Mathias Ekstedt. 2018. A Meta Language for Threat Modeling and Attack Simulations. In Proceedings of the 13th International Conference on Availability, Reliability and Security (ARES '18). Association for Computing Machinery, New York, NY, USA, Article 38, 1–8. https://doi.org/10.1145/3230833.3232799

- Wojciech Wideł, Simon Hacks, Mathias Ekstedt, Pontus Johnson, Robert Lagerström, The meta attack language - a formal description, Computers & Security, Volume 130, 2023, 103284, ISSN 0167-4048, [https://doi.org/10.1016/j.cose.2023.103284](https://doi.org/10.1016/j.cose.2023.103284)



