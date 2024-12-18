# Docker Build Failure: Missing Dependencies
This repository demonstrates a common error in Dockerfiles: failure to include necessary dependencies in the base image.

The original `Dockerfile` attempts to install `python3` and `pip` on top of `ubuntu:latest`. However,  `ubuntu:latest` might not have all the required build-time dependencies causing the `pip3 install` command to fail. 

The `Dockerfile-fixed` provides a solution by using a more appropriate base image with python pre-installed, avoiding this issue.