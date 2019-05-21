FROM ubuntu:latest

RUN apt-get update

# Install git, process tools
RUN apt-get -y install git procps

# Install build dependency
RUN apt-get -y install build-essential gdb cmake ncurses-dev libncurses5-dev libpcre2-dev gettext

# Install test dependency
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install expect vim-common locales && \
    locale-gen en_US.UTF-8

# Install lint dependency
RUN apt-get -y install clang cppcheck clang-format iwyu

# Clean up
RUN apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*
