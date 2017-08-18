# bdd-docker
bdd in a docker container

## Behavior-driven-development:
A framework for performing BDD-style development/testing using python's behave package.

This container includes:
 - anaconda (python version 2.7.xx)
 - - behave package
 - - selenium package
 - - xvfbwrapper package
 - xvfb
 - firefox
 - geckodriver

This container is intended to allow for rapid bdd setup and testing.
All the user has to do is utilize a volume mount to supply his/her bdd features and step files.

##	Running the container:
Assuming you have your tests in /home/user/features

$ docker run -v /home/user/features:/home/dev/features --rm --name bdd dockerdon60/bdd behave

This will run the tests and put any output into your /home/user/features folder.
