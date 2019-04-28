---
layout: event
image: /images/events/galaxy/workshop.png
tags: [Galaxy@Europe, hackathon, training]
title: 'Galaxy training and hackathon at Roscoff/France'
description: 'April, 23-26, 2019'
starts: 2019-04-23
ends: 2019-04-26
location:
  city: Roscoff
  region: Brittany
  country: France
supporters:
  -  ELIXIR Galaxy Community
photos:
  name: Bérénice Batut
  license: Copyright 2019
---

The [ELIXIR Galaxy Community](https://elixir-europe.org/communities/galaxy) organized a 4-days workshop at Roscoff (France) related to Galaxy tool integration and training.

More information [here](https://galaxyproject.eu/event/2019-01-28-roscoff-workshop/)

## [Participants](https://docs.google.com/presentation/d/1zY-Soc3ZIB9xg8OIdZItpt47rd7z0a6gWm_3esfaBps/edit#slide=id.g56a4b91dde_0_143)

{% include event-images.html images="
  /images/events/galaxy/roscoff_group.jpg"
%}



## Galaxy training

During the first day, we learned about the integration of high-quality tools within Galaxy with their dependencies (Bioconda, Planemo) using the IUC best practice guidelines. 
We also learned how to use Galaxy as a training tool and develop training material for the Galaxy Training Network.

{% include event-images.html images="
  /images/events/galaxy/galaxy_classroom_roscoff.jpg"
%}


## Hackathon

The second half of the workshop was dedicated to Hackathon sessions where we were able to bring our own project around 
tool integration and/or training material and develop them collaboratively, with the support of community experts.

### NordicESMHub project

[NordicESMhub](https://github.com/NordicESMhub) initiative aims at sharing knowledge, tools and resources to 
study the Earth’s climate and the regional impact of global changes in the Nordic countries  
(Denmark, Finland, Sweden, Iceland, Estonia, Norway).

The development of this project is mentored by [Bérénice][link_BereniceBatut] as part of the 
[Mozilla Open Leaders](https://foundation.mozilla.org/en/opportunity/mozilla-open-leaders/) 
[Round 7](https://foundation.mozilla.org/en/opportunity/mozilla-open-leaders/round-7/).

See our [roadmap](../roadmap.md) to get more information.

Our objective for the hackathon was to integrate Climate tools into 
[Galaxy Toolshed](https://toolshed.g2.bx.psu.edu/). Before the hackathon, the climate community was
not represented in the Galaxy Community and no tools related to climate Analysis were available.

#### What we did before the hackathon

We had two major objectives for the hackathon:

- Publish at least one simple tool in the [main Galaxy toolshed](https://toolshed.g2.bx.psu.edu)
- Learn how to create complex tools for Galaxy, especially where there is no [conda](https://anaconda.org/) 
package available

##### Simple python tools

To be ready, we chose to develop 4 simple tools in python:

- [psy-maps](https://github.com/NordicESMhub/galaxy-tools/tree/master/tools/psy-maps): make simple geographical plots from
latitude/longitude [netCDF](https://www.unidata.ucar.edu/software/netcdf/) data with the possibility to 
change the [projection](https://scitools.org.uk/cartopy/docs/latest/crs/projections.html). The tool uses
[psyplot-map](https://psyplot.readthedocs.io/projects/psy-maps/en/latest/) and creates a [png](https://en.wikipedia.org/wiki/Portable_Network_Graphics)
 image.
- [zonal statistics](https://github.com/NordicESMhub/galaxy-tools/tree/master/tools/mean-per-zone): This tool allows to compute zonal 
statistics from geospatial raster data based on vector geometries (shapefile). The raster input file must be 
in netCDF format with geographical coordinates (latitudes, longitudes) with the same coordinate reference 
system as the shapefile.
- [Shift longitudes](https://github.com/NordicESMhub/galaxy-tools/tree/master/tools/shift-longitudes): The wrapper aims at providing a simple utility 
to shift longitudes ranging from 0. and 360 degrees to -180. and 180. degrees. The input file must be in netCDF format with geographical coordinates (latitudes, longitudes) given in degrees.
- [Volcanoes of the World (VOTW) Database](https://github.com/NordicESMhub/galaxy-tools/tree/master/tools/smithsonian-volcanoes): Retrieve data from smithsonian volcanoes database
This tools creates an output file (csv or geojson format) with data retrieved from [VOTW database](https://volcano.si.edu/gvp_votw.cfm) using the selected typename. 
By default, the output format is csv (Comma-Separated Values). This setting can be changed by selecting another output format.


When arriving to the hackathon, these 4 python tools were ready i.e. developed and tested with test data. 


We also did our homework and started to create `xml` wrappers for Galaxy. For this we got help from 
[Bérénice][link_BereniceBatut] and the [Galaxy Training materials](https://training.galaxyproject.org/) on 
[tool developments](https://training.galaxyproject.org/training-material/topics/dev/tutorials/tool-integration/slides.html#1). All our Galaxy tools are
in our [galaxy-tools](https://github.com/NordicESMhub/galaxy-tools) repository. 

[Björn Grüning][link_BjornGruning] also kindly added [Travis Continuous Integration](https://travis-ci.org/) to 
get ready for automating tests and publishing to [Galaxy toolshed](https://toolshed.g2.bx.psu.edu/). 

All our tools were failing... And this is how we started our hackathon in Roscoff/France!
 
##### More complex tool: Community Earth System Model (CESM)
 
And we also chose [CESM](http://cesm.ucar.edu) as a more complex tool to be integrated in Galaxy. The
Community Earth System Model is a very important model for us because it is used for 
[Climate Model Intercomparison Project Phase 6](https://www.wcrp-climate.org/wgcm-cmip/wgcm-cmip6) and is one
of the most known model used for predicting climate and assessing climate changes.

The [Norwegian Earth System Model](https://noresm-docs.readthedocs.io/en/latest/) is derived from CESM,
sharing most of its code and used to assess regional impact of climate changes in the Nordic countries.
If we manage to integrate CESM in Galaxy, we would also be able to run NorESM in Galaxy! 

We usually run CESM/NorESM on [Norwegian HPC](https://www.sigma2.no/content/high-performance-computing-0) using
intel compilers. However, for small configurations and for teaching purposes, using HPC is an overkill. It adds
unnecessary complexity and makes it difficult for new users to focus on Science. We therefore started to
compile and run simple configuration (2 degrees resolution) on 
[IaaS Cloud](http://docs.uh-iaas.no/en/latest/) that we have at the [University of Oslo](https://www.uio.no/).

We managed to compile and run CESM on small Virtual Machines (Ubuntu 18.04, Centos 7) with 32 processors and 
64 GB. It is to be noted that we could not use [WACCM](https://www2.acom.ucar.edu/gcm/waccm) because it requires
128GB of memory. We tried to create a [Docker container](https://github.com/NordicESMhub/containers) but never managed
to make it work properly.

#### What we achieved during the hackathon

##### Flake8 compliance

Many of our python tools were not suitable for Galaxy Toolshed publishing because of 
[flake8](http://flake8.pycqa.org/en/latest/). Flake8 is a python package for checking python codes
 against coding style (PEP8), programming errors (like “library imported but unused” and “Undefined name”) 
 and to check cyclomatic complexity.
 
That is a bit cumbersome to fix afterwards and for our future developments, we would enforce it from the start. If your
favourite editor is [Atom](https://atom.io/) as editor, you can add 
[Atom linter plugin for Python, using flake8](https://atom.io/packages/linter-flake8).  

##### New datatypes in Galaxy for the Climate Community

Many of our data is encoded in [hdf5](https://www.hdfgroup.org/solutions/hdf5/), 
[netCDF](https://www.unidata.ucar.edu/software/netcdf/), [geoJSON](http://geojson.org/) and 
[shapefile](https://wiki.openstreetmap.org/wiki/Shapefiles).

We were quite lucky because both hdf5 and netCDF datatypes were already included in Galaxy and therefore ready
to be used.

[Björn][link_BjornGruning] added [geoJSON](http://geojson.org/) and 
[shapefile](https://wiki.openstreetmap.org/wiki/Shapefiles) datatype in Galaxy is 
[in progress](https://github.com/galaxyproject/galaxy/pull/7819).

##### New conda package and docker/Singularity containers for the Climate Community

In fact, the easiest is always to add your tool to conda. Adding [CESM](https://anaconda.org/bioconda/cesm) to
[bioconda](https://bioconda.github.io/) channel is a major achievement for us. 

It seems a bit controversial for the Climate Community to use bioconda but when we understood that we would 
also get a [docker/singularity container](https://quay.io/repository/biocontainers/cesm) for "free" i.e. 
without any additional efforts, then we were easily convinced...

The most amazing thing is that you only need to create [two files](https://github.com/bioconda/bioconda-recipes/tree/master/recipes/cesm) to get your package in bioconda and the
associated docker/singularity container! Once a day, docker/singularity containers are automatically 
created for all new bioconda packages. 

To install cesm using bioconda:

~~~`bash`
conda install -c conda-forge -c bioconda cesm 
~~~

We have successfully used the new cesm bioconda package on our Virtual Machines. The performance is exactly
the same as if we compile with the GNU compiler. 

We also successfully used the new cesm bioconda package on [Fram](https://documentation.sigma2.no/quick/fram.html), 
the current largest HPC in Norway. Our run was about 30% slower than when we compile CESM on Fram with the 
Intel compiler. There are many things that can explain this drop in performance but our first thought is linked
to HDF5: we usually use parallel HDF5 when compiling CESM while in bioconda, HDF5 is not parallel. 
Of course, we need to perform more tests and anyway, being able to run small configuration on the cloud is
definitely a huge achievement for us!

We also started to create the corresponding CESM xml wrapper to add CESM as a new Galaxy tool. We are really looking forward to it.
Thanks to the hackathon, there is no technical obstacle anymore; it's on us!

Thanks [Björn][link_BjornGruning] for adding CESM to bioconda!

##### New Climate Analysis Tools in Galaxy Toolshed

A little bit like magic...  A new category **[Climate Analysis](https://toolshed.g2.bx.psu.edu/)** appeared 
in Galaxy Toolshed! Having a team of Galaxy Experts makes everything so much easier! 

Getting our simple python tools flake8 compliant was the first step. Then we also needed to link properly 
our [galaxy-tools](https://github.com/NordicESMhub/galaxy-tools) repository to Travis by:

- Creating an account in the [Galaxy Toolshed](https://toolshed.g2.bx.psu.edu) and [Galaxy Test Toolshed](https://testtoolshed.g2.bx.psu.edu) for the Climate Community.
- Defining two environment variables:
	- `SHED_EMAIL`
	- `SHED_PASSWORD`

And after many `planemo test` and `planemo server`, we successfully published 3 new tools in the Galaxy Toolshed:

- psy_maps and shift_longitudes are both published in the Repositories in Category Climate Analysis
- mean_per_zone is published in the Repositories in Category GIS

We did not managed to publish [smithsonian-volcanoes](https://github.com/NordicESMhub/galaxy-tools/tree/master/tools) 
because the python code still has some problems (names of icelandic volcanoes contain characters that are not utf-8) but
being able to publish 3 new tools in the Galaxy Toolshed and more importantly having the framework for publishing
new tools made our day!

[link_AnneFouilloux]: https://github.com/annefou
[link_BereniceBatut]: http://bebatut.fr/
[link_BjornGruning]: https://github.com/bgruening