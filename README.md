# Code_Aster Singularity Recipe

A basic template/test Singularity recipe for Code_Aster and dependencies.
See here: https://www.code-aster.org/spip.php?article272 for more details.

## Interactive Build of Container

Once you've installed Singularity, `cd` to the directory you want to store your container and enter the following command to create the container:

```bash

sudo singularity build --sandbox <name_of_container> docker://ubuntu:18.04

```

To enter this container and start installing software, enter the following command:

```bash

sudo singularity shell --writable <name_of_container>

```

You can now start building your container by following the simple recipe file I've provided, so step one would be:

```bash

apt-get -y update

```

Followed by:

```bash

apt-get install -y build-essential
apt-get install -y cmake
...

```
