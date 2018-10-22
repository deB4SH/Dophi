# Dophi
A docker container for the rimworld phi server.
You can get the container with the following command `docker pull docker.0x09.de/deb4sh/dophi:1.0`.
This images is build on top of an alpine image with mono 5.14 preinstalled. It also includes glibc for further support of environments.


# Container Informations
The phi server communicates on port `16180` by default, which is mounted by the maven environment to `62001`. If you're creating yourself an container based on that image keep in mind to bind that specific port.
Due to the fact that the server wont save any informations there is no data mounted to the outside.