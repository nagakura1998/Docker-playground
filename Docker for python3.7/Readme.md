1. Build image\
docker build ./
2. Run docker bind mount, a file or directory on the host machine is mounted into a container\
docker run -it -v [absolutePathToHostFolder]\src:/usr/src/app/test [imageID] bash
