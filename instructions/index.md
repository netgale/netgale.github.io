---
layout: page
title: Instructions
---
## Requirements
- The offline CPU version only requires Java 8 and 4 GB of RAM.
- The offline GPU version requires opencl etc.
- The online GPU version requires an API key from ...

## Getting the plugin
- Download the [plugin](/downloads)

- Download and unpack the [example networks](/downloads/example_networks.zip)

## Setup for Cytoscape 3
- Open "App Manager" from the menu bar:

{% img /img/tutorial/menubarappmanager.png %}

- Choose "Install from file"

{% img /img/tutorial/appmanager.png %}

- NETGALE should now be loaded and visible in the "Control Panel":

{% img /img/tutorial/controlpanel.png %}

## Loading the example networks

- Press the "Import Network From File" button in the menu bar:

{% img /img/tutorial/iconbar.png %}

- Choose the first example network:

{% img /img/tutorial/networksfilemanager.png %}

- Ensure that "Network Collection" is set to "Create new network collection"

{% img /img/tutorial/importnetwork.png %}

- Repeat this for the 2 other network files, each time ensuring "Create new network collection" is set as "Network Collection"

- You can then layout each of the networks using the "Apply Prefered Layout"-button

{% img /img/tutorial/prefuse.png %}

- Cytoscape should now look something like this:

{% img /img/tutorial/networksloadedoverview.png 1200 %}

## Basic Usage

- Start by doing a simple local cpu alignment of the 3 networks by pressing the start button:

{% img /img/tutorial/startbasic.png %}

- A progress bar will show up:

{% img /img/tutorial/progressbar.png %}

- The result is a consensus network showing largest connected common subgraph found

{% img /img/tutorial/consensus.png %}

- Repeat the result with exceptions by typing 1 in the "exceptions" field

{% img /img/tutorial/exceptions.png %}

## Advanced Usage

### Similarity file

- An external similarity file can be loaded. This is used improve the solution in a non-topological direction. Please note that the similarities will be normalized to the range [0,1] 

Factor
: The weight of the similarity information.

Minimum
: Minimum value to use from the file for normalization. If none is chosen, the minimum value in the file will be used.

Maximum
: Maximum value to use from the file for normalization. If none is chosen, the maximum value in the file will be used.

{% img /img/tutorial/similaritytab.png %}

### Parameters

Ants
: Determines the amount of ants used in the aco. More ants will improve etc...

Alpha
: Determines the the importance of the pheromone value. A high value will increase converge towards a solution.

Beta
: Determines the heuristic factor, in this case graphlet which only uses topological information to produce the solution.

Evaporation rate
: Determines the speed of pheromone evaporation. If a path is seldom visited its pheromone level will decrease. A higher value increases convergence.

{% img /img/tutorial/parameterstab.png %}
