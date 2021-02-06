---
layout: event
image: /images/events/coderefinery/workshop.png
tags: [ines, coderefinery, hackathon, training]
title: 'First joint INES and CodeRefinery hackathon'
description: 'February, 05, 2020'
starts: 2020-02-05
ends: 2020-02-05
location:
  city: Oslo/Bergen/online
  region: Nordic countries
  country: Nordic countries
supporters:
  - INES
  - CodeRefinery
photos:
  name: CodeRefinery Copyright
  license: CodeRefinery license
---

<img src="https://coderefinery.org/processed_images/95d96b4244c1bab700.png" width="30%"> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://www.mn.uio.no/geo/english/research/projects/ines/bilder/ines-250px.jpg">

This hackathon is organized by [CodeRefinery](https://coderefinery.org/) and [INES](https://www.norceresearch.no/prosjekter/infrastructure-for-norwegian-earth-system-modelling-ines).

# Registration

To get an idea about how many people will be coming, we kindly ask you to register [here](https://docs.google.com/forms/d/e/1FAIpQLSfXqBkzOGWvK6kuLUlDMJ2viFBCwEUSfOWjpyXHohSL8ncnsA/viewform).

For the first INES hackathon, we have chosen to work on four topics.

<ul>
<li><a href="#topic-1">Topic-1:documentation</a></li>
<li><a href="#topic-2">Topic-2: norESM code structure</a></li>
<li><a href="#topic-3">Topic-3: norESM input data</a></li>
<li><a href="#topic-4">Topic-4: norESM model outputs</a></li>
</ul>

<br>

<h2 id="topic-1"></h2>

## Topic-1: documentation

#### Mentor: Michael (Oslo)

#### Goal:

This group will work on the norESM documentation. The main objective is to update the norESM documentation to help:

- new users to get the code and run norESM supported configurations
- developers to understand on how to contribute to norESM code developments
- anyone to contribute to the norESM documentation
	
#### Expected outcome:

- Restructured documentation for noresm 2.5 in [https://github.com/NorESMhub/noresm/doc](https://github.com/NorESMhub/noresm/doc) fully tested locally and ready to be deployed.

#### Who do we need in this group

- Anyone willing to run norESM or having an experience on how to run norESM.
- Documentation is written in plain English.

<h2 id="topic-2"></h2>
## Topic-2: norESM code structure

#### Mentors: Mats (Bergen), Anne (Oslo)

#### Goal:

The current [norESM code](https://github.com/metno/noresm-dev) does not follow CESM structure:
- we have two private repositories [noresm](https://github.com/metno/noresm) and [noresm-dev](https://github.com/metno/noresm-dev) hosted on github in metno github organization.
- we gave all the components (including cime coupler) in the noresm repository

So the goal of this group is to use [https://github.com/NorESMHub/noresm](https://github.com/NorESMHub/noresm) and follow CESM code structure (along with documentation, link components through manage externals).

#### Expected outcome:

- Get a running (though probably incomplete) NorESM2 based on externals

#### Who do we need in the group

- representant of each component (ocean, atmosphere, land, etc.)
- norESM model developers
- git expertise

<h2 id="topic-3"></h2>
## Topic-3: norESM input data

#### Mentor: Jan

#### Goal:

To be able to run a norESM case on another machine, one needs to have the corresponding norESM inputs. The goal of this group is to make sure anyone can get norESM inputs on any machines for runnin all the norESM supported configurations.

#### Expected outcome:

- Thredds or ftp server on nird containing basic input files not from CESM
- Updated scripts for running the model from fram, vilje and eg UiO machine

#### Who do we need in this group

We put a list of desirable expertise (you need to have at least one of them!):

- experience in running norESM
- knowledge of a scripting language (bash and/or python)

Access to virtual machines will be provided for testing.

<h2 id="topic-4"></h2>
## Topic-4: norESM model outputs

#### Mentor: Yanchun

#### Goal:

The goal is to review all the procedure for publishing norESM model outputs (cmorisation, policy for deleting experiments, archiving and long-term preservation).


#### Expected outcome:

- Revisited cmorisation script, documentation
- Clean up procedure with script to find data per user
- Procedure for saving and documenting model experiments
- Overview of data which could be 

#### Who do we need in this group

- users running norESM experiments
- users analyzing their norESM model outputs
- data management experts
- cmorisation experts

<p>Photo by <a href="https://unsplash.com/@rayhennessy">Ray Hennessy</a> on <a href="https://unsplash.com/">Unsplash</a>.</p>


