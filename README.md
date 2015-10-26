# docker-ijulia

#No working at the moment because of change of ubuntu/julia and jupyter .. tring to fix it.

docker container for [IJulia Notebook][3]

"IJulia is a [Julia-language][6] backend combined with the [IPython][7] interactive environment (soon to be called [Jupyter][8]). This combination allows you to interact with the Julia language using Jupyter/IPython's powerful [graphical notebook][9], which combines code, formatted text, math, and multimedia in a single document"

This notebook is for the last version in development for Julia if you are looking for the stable version I recomended that used the official docker image from Jupyter:  [jupyter/datascience-notebook][11]   and for more jupyter [docker-stacks][12]

## Install dependencies

  - [Docker][2]

To install docker in Ubuntu 14.04 use the commands:

    $ sudo apt-get update
    $ wget -qO- https://get.docker.com/ | sh

 To install docker in other operating systems check [docker online documentation][4]

## Usage

To run container use the command below:

    $ docker run -d -p 8998:8998 quantumobject/docker-ijulia

Run the after install script:

    $ docker exec -it container_id /sbin/after_install

Need to provide new password and info to generate ssl for access web interface of IJulia.

## Accessing the IJulia applications:

After that check with your browser at addresses plus the port 8998:

  - **https://host_ip:8998/**

To access the container from the server running docker :

    $ docker exec -it container_id /bin/bash

## More Info

About [IJulia][1]

To help improve this container [docker-ijulia][5]

For additional info about us and our projects check our site [www.quantumobject.com][10]

[1]:https://github.com/JuliaLang/IJulia.jl
[2]:https://www.docker.com
[3]:https://github.com/JuliaLang/IJulia.jl
[4]:http://docs.docker.com
[5]:https://github.com/QuantumObject/docker-ijulia
[6]:http://julialang.org
[7]:http://ipython.org
[8]:http://jupyter.org
[9]:http://ipython.org/notebook.html
[10]:http://www.quantumobject.com
[11]:https://github.com/jupyter/docker-stacks/tree/master/datascience-notebook
[12]:https://github.com/jupyter/docker-stacks
