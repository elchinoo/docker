Dockerfiles
==================

This repository provides Dockerfiles for use on development environment. I'll use popular implementations as base images and they are mostly stable but it's not intended to be used in production though.

## Contribution Guidelines

Each Dockerfile should contain a README that includes the following:

 * Version of OS and Docker that it was built/tested against
 * Instructions for building the Docker image

--
    For example: docker build --rm=true -t my/image .
--

 * Instructions for running the image, including examples for persistent data, port mapping, etc.
 * Examples for testing and/or validating the functionality of the image.
 * Do not include executable scripts. Provide them and mark them as executable in the Dockerfile

--
    ADD ./script.sh /usr/bin/
    RUN chmod -v +x /usr/bin/script.sh
--

 * If creating a container for a specific language, specify the version of that language.
 * If any download or package manager is used during the build process, run a clean up process afterwards to reduce the image size.

## Notes

This readme file is based on CentOS project and can be found in https://github.com/CentOS/CentOS-Dockerfiles/blob/master/README.md

Known issues:

 * None at this time.
