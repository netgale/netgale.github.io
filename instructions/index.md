---
layout: page
title: Instructions
---
## Requirements

* The offline CPU version only requires Java 8 and 4 GB of RAM.
* The offline GPU version requires opencl etc.
* The online GPU version requires an API key from ...

## Getting the plugin

Download the [plugin](/downloads)

Download and unpack the [example networks](/downloads/example_networks.zip)

## Setup for Cytoscape 3

Open "App Manager" from the menu bar:

![](/img/tutorial/menubarappmanager.png){: .img-responsive }

Choose "Install from file"

![](/img/tutorial/appmanager.png){: .img-responsive }

NETGALE should now be loaded and visible in the "Control Panel":

![](/img/tutorial/controlpanel.png){: .img-responsive }

## Loading the example networks

Press the "Import Network From File" button in the menu bar:

![](/img/tutorial/iconbar.png){: .img-responsive }

Choose the first example network:

![](/img/tutorial/networksfilemanager.png){: .img-responsive }

Ensure that "Network Collection" is set to "Create new network collection"

![](/img/tutorial/importnetwork.png){: .img-responsive }

Repeat this for the 2 other network files, each time ensuring "Create new network collection" is set as "Network Collection".

You can then layout each of the networks using the "Apply Prefered Layout" button

![](/img/tutorial/prefuse.png){: .img-responsive }

Cytoscape should now look something like this:

![](/img/tutorial/networksloadedoverview.png){: .img-responsive }

## Basic Usage

Start by doing a simple local cpu alignment of the 3 networks by pressing the start button:

![](/img/tutorial/startbasic.png){: .img-responsive }

A progress bar will show up:

![](/img/tutorial/progressbar.png){: .img-responsive }

The result is a consensus network showing largest connected common subgraph found

![](/img/tutorial/consensus.png){: .img-responsive }

Repeat the result with exceptions by typing 1 in the "exceptions" field

![](/img/tutorial/exceptions.png){: .img-responsive }

## Advanced Usage

### Similarity file

An external similarity file can be loaded. This is used improve the solution in a non-topological direction. Please note that the similarities will be normalized to the range [0,1] 

Factor
: The weight of the similarity information.

Minimum
: Minimum value to use from the file for normalization. If none is chosen, the minimum value in the file will be used.

Maximum
: Maximum value to use from the file for normalization. If none is chosen, the maximum value in the file will be used.

![](/img/tutorial/similaritytab.png){: .img-responsive }

### Parameters

Ants
: Determines the amount of ants used in the aco. More ants will improve etc...

Alpha
: Determines the the importance of the pheromone value. A high value will increase converge towards a solution.

Beta
: Determines the heuristic factor, in this case graphlet which only uses topological information to produce the solution.

Evaporation rate
: Determines the speed of pheromone evaporation. If a path is seldom visited its pheromone level will decrease. A higher value increases convergence.

![](/img/tutorial/parameterstab.png){: .img-responsive }
