## Welcome to the home of the Meta Attack Language (MAL)

### What is MAL?
MAL is a language for creating for creating domain-specific threat modeling languages - a malLang. MAL could be thout of as a framework for combining systems modeling such as UML with attack graphs. More precisely, MAL formalizes how to generate attack graphs from system model specifications. In a malLang you specify Asset categories (e.g. computers, applications, networks, data), how they are allowed to be related (e.g. computers can _run_ applications and be _connectedTo_ networks), what attack actions that are possible to perform on the respective Assets (e.g. we can _connect_, _authenticate_, _guessCredentials_, and _compromise_ computers) as well as what successful attack action would enable atempting new actions (e.g. after succeeeding to connect to a computer you can either authenticate -if you have credentials- or guess the credentials. If either of these actions are sucessful you will have compromised the computer and you will be able to connect to all other computers located on the same network as the compromised computer.) Depending on how system assets are configured in an instance model -what the system architecture look like- this will thus determine what attack vectors are possible according to the domain-specific language and express them in an attack graph.    

### Why MAL?
With MAL it is possible to encode cybersecurity competence so that it can be reused for many system environements. Cybersecurity experts can describe how systems can be attacked and also defended, and this knowledge can be applied by system designers and maintainers for analyzing their particular system environement. MAL thus enables the construction of a digital twin for cybersecurity in which red team simulations can be made at scale. In addition the effect of blue team intervensions can be studied. This can be used for traditional threat modeling and security analysis identifying effective security design, but also for operations guiding protective actions given the observation of some particular attack chain. Moreover, the MAL asset graphs and attack graphs can also be used as a simulation infrastructure for simulation-based training of attacker and defender agents, for instance throuch machine learning.

## MAL resources
MAL has been developed by Software Systems Architecture and Security group at KTH Royal Institute of Technology in Sweden and this repo gathers results of many of the various projects that the research groups has been working on over the years.    

