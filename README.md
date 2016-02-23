# Alpine Linux with glibc compatibility layer installed

# Summary

- C library installed on the Alpine Linux base image, enabling binaries to run which link to glibc libs 
- Provides a super small image to run C based executables upon
- Intended for use as the FROM image in your Dockerfile danielwhatmuff/alpine-glibc-docker
- glibc provided by the Github project [alpine-pkg-glibc](https://github.com/andyshinn/alpine-pkg-glibc)

[![](https://badge.imagelayers.io/danielwhatmuff/alpine-glibc-docker:latest.svg)](https://imagelayers.io/?images=danielwhatmuff/alpine-glibc-docker:latest 'Inspect Docker images at imagelayers.io')

# Requirements

- Docker :whale: - if you are on Mac, checkout the [Docker Toolbox](http://docs.docker.com/mac/step_one/)

# To build the Docker image

- Clone the repo
```bash
git clone https://github.com/danielwhatmuff/alpine-glibc-docker.git
```
- Build the image using docker
```bash
$ docker build -t glibc .
```

# Alternatively, you can pull the Docker Hub automated build

```bash
$ docker pull danielwhatmuff/alpine-glibc-docker
```

# Or use as the FROM image in your Dockerfile

```bash
FROM danielwhatmuff/alpine-glibc-docker

RUN curl -o /usr/bin/some-c-program http://download.example.com/some-c-program

...
```

### Contributing
File issues in GitHub to report bugs or issue a pull request to contribute.
