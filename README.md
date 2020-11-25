**This repository is only here for historical reasons. The Docker files were
integrated into the main repository in late 2020.**

This repository contains a Dockerfile template for containers used to test
[qutebrowser](https://www.qutebrowser.org/) on CI.

The `generate.py` script uses that template to generate various image
configuration.

The images are rebuilt via Github Actions in this repository, and qutebrowser then
downloads them during the CI run in the qutebrowser repository. Note that
means that it'll take a while until builds will use the newer image if you make
a change to this repository.
