FROM ubuntu:latest
LABEL maintainer="imelnych"

# prerequisites for valgrind
RUN apt-get update -y
RUN apt-get install -y build-essential valgrind vim

WORKDIR /app
CMD /bin/bash

###### CHECK ######
# docker build -t valgrind-image .
# docker run --rm -it valgrind-image
# compile any c file and run
# valgrind --leak-check=yes a.out