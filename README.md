This repository contains Dockerfiles for containers used to test
[qutebrowser](https://www.qutebrowser.org/) on Travis CI.

The images are rebuilt on [Docker Hub](https://hub.docker.com/) and
qutebrowser then downloads them during the Travis run. Note that means that
it'll take a while until builds will use the newer image if you make a change
to this repository.
