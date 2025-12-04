# STEMgraph - Graph based STEM Training
STEMgraph is a project, started to provide a different kind of learning experience.
It organizes challenges in a graph oriented database.
The goal of this project is, to provide an improved way for autodidacts and support students in STEM-fields by providing clear paths forward.

## Philosophy
Science, Technology, Engineering and Math are more than just Big-Bang-Theory look-alike folks sitting in an office in front of a whiteboard, coming up with great ideas.
Ingenuity is definitely helpful, but from our perspective, a great part of it is simply a craft that can be trained.
We even believe that without the proper training in the crafts, no amount of ingenuity will make you go very far in your academic life.
STEMgraph is designed to provide a path through the forest of handy skills you can use to navigate your own endeavors in STEM. 

We at STEMgraph see the process of learning as a journey through a graph.
The basic nodes in this graph are skills.
You may only learn a specific skill if you have already learned the necessary prerequisites, making it a directed graph.
Specific collections of achieved skills constitute a profession.
Every profession can be expressed in terms of a set of skills and a set of values and beliefs.
It is not in STEMgraph's scope to teach the values and beliefs, but just the skills.
Therefore, STEMgraph doesn't aim to replace a university education, but rather try to extract the skill-training from universities and make them a place for discussing these crafts.

## Process
STEMgraph starts with a basic root node of skill: "The scholar can read the English language".
From there, the completion of challenges takes the scholar to new nodes.
The challenges are also saved inside the graph database.
Every challenge in the database holds a reference to a git repository with the description of the challenge to complete in order to learn the next skill.
Every challenge is also linked to a preconfigured ChatGPT session via a sharing link.
The scholar can upload their solution to this session and let ChatGPT examine the solution. 

## Implementation
The graph database is implemented in a server-side container.
It changes its form from time to time until there is a stable release.
All challenges are stored in this GitHub organization as individual repos and are meant to be as atomic as possible.
The cached database gets filled automatically by parsing the GitHub organization.
This means each challenge should teach one skill at best.
A challenge that needs multiple steps to be completed is divided into `tasks`.
Each of the repos shall contain:
* a UUID as unique identifier of the challenge
* a License, set by the original author of the challenge
* a file called `README.md`
* if necessary, a directory called `assets/` for figures etc.
* metadata provided in JSON

A map of the graph can be seen at http://stemgraph.boekelmann.net

## Contact
If you need help working your way through STEMgraph, want to discuss certain topics, use STEMgraph for your own teaching or contribute, [join the "Full-Stack-Engineering" Discord Server and join our discussions](https://discord.gg/rdwVGj4mzD)!
