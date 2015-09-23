# atomci

Use docker-compose to setup a Atom Container and CI pipeline components

*** This is a work in progress. ***

The plan is to use docker-compose to create a complete scaled-down CI pipeline which can be managed directly from Atom.

The Pipeline would consist of the following containers :

Atom : Used as is or with pre-baked packages installed. There are a number of terminal and shell packages that allow the user to

run scripts or terminal commands.  In the compose file the docker and docker-compose commands are shared into the Atom container.

Build : TBD

unittest  : TBD

systemtest  : TBD

Jenkins Slave : TBD

 
What is the point of creating a scaled-down CI infrastructure ?

A major challenge, even after the introduction of Docker, is the orchestration of the containers and complex run commands.

docker-compose allows us to ship a fully configured CI environment which developers can run locally and which will be identical

to the environment we use in our production CI.

How simple can we make this ?

The plan is that we create a docker and docker-compose atom package which gives the user a more integrated solution.


Why use docker-compose ?

- Simplifies the creation and management of multiple containers

- No more long docker run commands

- All container config within one file

- Simple to install
