
FROM ubuntu:20.04
RUN apt-get install -y update
RUN apt-get install -y build-essential
RUN apt-get install -y libgtest-dev
RUN apt-get install -y cmake
RUN cd /usr/src/gtest
RUN cmake CMakeLists.txt
RUN make
RUN cp *.a /usr/lib

COPY to-be-copied sample

RUN cmake CMakelists.txt
make
COPY to-be-copied sample
./runTests