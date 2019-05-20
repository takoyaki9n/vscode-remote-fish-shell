FROM ubuntu:latest

RUN apt-get update

# Install git, process tools
RUN apt-get -y install git procps

# Install build dependency
RUN apt-get -y install build-essential gdb cmake ncurses-dev libncurses5-dev libpcre2-dev gettext cppcheck valgrind

# Clean up
RUN apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*
