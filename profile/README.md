# STEMgraph - Graph based STEM Training
STEMgraph is a project, started to provide a new type of learning experience.
It organizes skills, tasks and professions in a graph oriented database management system.
The goal of this project is, to provide an improved way for autodidacts and support students in STEM-fields by providing clear paths forward.

## Philosphie
Science, Technology, Engineering and Math are more than just Big-Bang-Theory look-alike folks sitting in an office in front of a whiteboard, coming up with great ideas. 
Ingenuity is definitly helpful, but from our perspective, a great part of it is simply a craft, that can be trained. 
We even believe, that without the proper training in the crafts, no amount of ingenuity will make you go very far in your academic life. 
STEMgraph is designed, to provide a path through the forest of handy-skills you can use to navigate your own endeavours in STEM. 

We at STEMgraph see the process of learning as a journey through a graph.
The basic nodes in this graph, are skills.
You may only learn a specific skill, if you have already learned the necessary prerequisits, making it a directed graph.
Specific collections of achieved skills, constitute a profession. 
Every profession can be expressed in terms of a set of skills and a set of values and believes. 
It is not in STEMgraphs scope to teach the values and believes, but just the skills. 

## Process
STEMgraph starts with a basic root node of skill: "The scholar can read the english language".
From there, the completion of challenge takes the scholar to new nodes. 
The challenges are also saved inside of the graph database.
Every challenge in the database holds a reference to a git-repository with the description of the challenge to complete in order to learn the next skill. 
Every challenge is also linked to preconfigured ChatGPT session via a sharing-link.
The scholar can upload their solution to this session and let ChatGPT examine the solution. 

## Implementation
The graph-database is implemented in neo4j, provided by AI-Gruppe.
All challenges are stored in this github organization as individual repos and are meant to be as atomic as possible. 
This means, each exercise should teach one skill at best, but never more than three. 
An exercise, that needs multiple steps to be completed is divided into `tasks`.
Each of the repos shall contain:
* a UUID as unique identifier of the challenge
* a Licence, set by the original author of the challenge
* a file called `README.md`
* if necessary a directory called `assets/` for figures etc.

## Contributing
If you want to contribute, please drop an email to 
```
sboekelmann@ep1.ruhr-uni-bochum.de
```
