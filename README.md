# atomci

*** This is a work in progress. Literally just threw this shit together. ***

## Aim : Use docker-compose to setup a Atom Editor (http://atom.io) for development and management of CI pipeline components

docker-compose simplifies the creation of a complete scaled-down CI pipeline which is portable, deployable and throwaway-able.  

The Pipeline would consist of the following containers :

Atom : Used as is or with pre-baked packages installed. There are a number of terminal and shell packages that allow the user to run scripts or terminal commands.  In the compose file the docker and docker-compose commands are shared into the Atom container.

Build : TBD.  Includes build tools needed to create artifacts such as documentation, rpms and containers.

unittest  : TBD. Includes all static analysis and unit test tools.

systemtest  : TBD. May include one or more containers which represents a environment for system testing.

Jenkins Slave : TBD

 
## What is the point of creating a scaled-down CI infrastructure ?

A major challenge, even after the introduction of Docker, is the orchestration of the containers and complex run commands.

docker-compose allows us to ship a fully configured CI environment which developers can run locally and which will be identical to the environment we use in our production CI.

## How simple can we make this ?

The plan is to create a docker and docker-compose atom package which gives the user a more integrated solution.  Using shortcuts and hotkeys to build, test and deploy code and containers from Atom in a container would be cool.


## Why use docker-compose ?

- Simplifies the creation and management of multiple containers

- No more long docker run commands

- All container config within one file

- Simple to install

Usage :

Install docker and docker-compose
See the docker-compose.yml file for comments on which options should be changed to suit your needs.

Start Atom Editor :

```
docker-compose up -d atom
```

When Atom is started you can install any of the terminal or shell packages.  The terminal-status package is simple to use and will allow you to run docker and docker-compose commands on the host.
