[![Build Status](https://travis-ci.org/qutebrowser/docker-travis.svg?branch=master)](https://travis-ci.org/qutebrowser/docker-travis)

This repository contains Dockerfiles for containers used to test
[qutebrowser](https://www.qutebrowser.org/) on Travis CI.

The images are rebuilt via Travis CI in this repository, and qutebrowser then
downloads them during the Travis run in the qutebrowser repository. Note that
means that it'll take a while until builds will use the newer image if you make
a change to this repository.
