# petalinux-docker

Copy petalinux-v2022.1-final-installer.run file to this folder. Then run:

`docker build --build-arg PETA_VERSION=2022.1 --build-arg PETA_RUN_FILE=petalinux-v2022.1-final-installer.run -t petalinux:2022.1 .`

After installation, launch petalinux with:

`docker run -ti --rm -e DISPLAY=$DISPLAY --net="host" -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/home/vivado/.Xauthority -v $HOME/Projects:/home/vivado/project  petalinux:2022.1 /bin/bash`
